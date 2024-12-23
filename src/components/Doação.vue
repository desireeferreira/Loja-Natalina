<script setup>
import maozinha from "../assets/maozinha.png"

</script>

<template>
<section class="conectar-generosidade">
    
     <div class="conectar-imagem">
    <img :src="maozinha" alt="imagem-maozinha">
    </div>
    <div class="container-secundario">
    <h3 class="titulo-conectar">Conectando generosidade ao redor do mundos</h3>
    <p class="descricao-conectar">Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
    <button @click="handleDonation" class="doacoes-botao">FAZER UMA DOAÇÃO</button>
    </div>
</section>
</template>
<style lang="scss">
.conectar-generosidade{
  display: flex;
  align-items: center;
  justify-content:center;
  flex-wrap: wrap;
  width: 100%; 
  height:auto;
  padding:20px;
  box-sizing: border-box;
  gap:20px;
  } 

.container-conectar{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    max-width: 600px;
    text-align: center;
    margin-bottom: 10px;
    padding: 20px;
  } 
.container-secundario{
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  max-width: 600px;
  
  padding:20px;
  box-sizing: border-box;
  text-align: center;
}
 .titulo-conectar{   
    font-size: 2rem;
    color: black;
    margin-bottom: 15px;
    text-align: center;
    line-height: 1.4;
    
} 

.descricao-conectar{  
      font-size: 1.2rem;
      margin-bottom: 20px;
      color: #333;
      line-height: 1.5;
            
}

.conectar-imagem {
  display:flex;
  justify-content: center;
  width: 100%;
  max-width: 400px;
  height: auto;  
  margin-bottom: 20px;
  
}
.doacoes-botao{
  padding: 10px 20px;
  font-size: 1rem;
  background-color: #d14b4b;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor:pointer;
  width:auto;
  max-width: 200px;
  
  &:hover {
    background-color: #b63939;
  }
}

@media (max-width: 768px) {
  .conectar-generosidade {
    flex-direction: column;
    padding: 10px;
    gap: 15px;
  }

  .container-secundario {
    width: 90%;
  }

  .titulo-conectar{
    font-size: 1.5rem;
  }

  .descricao-conectar{
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .titulo-conectar{
    font-size: 1.3rem;
  }

  .descricao-conectar{
    font-size: 0.9rem;
  }
  .doacoes-botao{
    font-size: 0.9rem;
    padding: 8px 16px;
  }

  .conectar-imagem{
    max-width: 300px;
  }
}
</style>