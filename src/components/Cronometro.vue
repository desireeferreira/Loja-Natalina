<script setup>
import presentes from "../assets/presentes.png"

import { ref, computed, onMounted, onUnmounted } from 'vue';


const christmasDate = new Date(new Date().getFullYear(), 11, 25, 0, 0, 0);


const days = ref(0);
const hours = ref(0);
const minutes = ref(0);
const seconds = ref(0);

let timer = null;

function updateTimer() {
  const now = new Date();
  const timeDifference = christmasDate - now;

  if (timeDifference <= 0) {
    clearInterval(timer);
    days.value = 0;
    hours.value = 0;
    minutes.value = 0;
    seconds.value = 0;
    return;
  }

  days.value = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
  hours.value = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  minutes.value = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
  seconds.value = Math.floor((timeDifference % (1000 * 60)) / 1000);
}


onMounted(() => {
  updateTimer();
  timer = setInterval(updateTimer, 1000);
});


onUnmounted(() => {
  clearInterval(timer);
});
</script>
<template>
 
<section class="tempo-limitado">
    <div class="container-oferta">        
    <h2 class="oferta-titulo">Tempo limitado</h2>
    <p class="oferta-descricao">Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
    <img :src="presentes" alt="">
</div>
  </section>
   
   <div class="contagem-regressiva">
        <div class="caixa-de-tempo">
          <span class="valor">{{ days }}</span>
          <span class="rotulo">Dias</span>
        </div>
        <div class="caixa-de-tempo">
          <span class="valor">{{ hours }}</span>
          <span class="rotulo">Horas</span>
        </div>
        <div class="caixa-de-tempo">
          <span class="valor">{{ minutes }}</span>
          <span class="rotulo">Minutos</span>
        </div>
        <div class="caixa-de-tempo">
          <span class="valor">{{ seconds }}</span>
          <span class="rotulo">Segundos</span>
        </div>
      </div>    
</template>
<style scoped lang="scss">

.tempo-limitado{
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    
}

.container-oferta{
    text-align: center;
}

.oferta-titulo{
    font-size: 2rem;
    color: #d14b4b;
    margin-bottom: 10px;
}
.oferta-descricao{
    font-size: 1.2rem;
      margin-bottom: 20px;
      color: #333;
}
.oferta-imagem {
      width: 200px;
      height: auto;
}

.contagem-regressiva {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 20px;
}

.caixa-de-tempo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.valor {
  font-size: 2rem;
  font-weight: bold;
}

.rotulo {
  font-size: 1rem;
  color: #555;
}

</style>