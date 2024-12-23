<script setup>
import logonatal from "../assets/logonatal.png";
import lojanatalina from "../assets/lojanatalina.png";

const handleDonation = () => {
  alert("Obrigada por sua doação!");
};
</script>

<template>
  <section class="natal-doacoes">
    <div class="doacoes-container">
      <img :src="logonatal" alt="Logo de Natal" class="doacoes-logo" />
      <h1 class="doacoes-titulo">
        Uma plataforma de <span>doação para espalhar alegria</span>
      </h1>
      <p class="doacoes-descricao">
        Nessas festas de fim de ano, mande um presente para a pessoa amada e
        compartilhe a alegria do Natal.
      </p>
      <button @click="handleDonation" class="doacoes-botao">
        Fazer uma doação
      </button>
    </div>

    <div class="loja-natalina">
      <img :src="lojanatalina" alt="Loja Natalina" />
    </div>
  </section>
</template>

<style scoped lang="scss">

.natal-doacoes {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #ffe9e8;
  height: 450px;
  padding: 20px;

  .doacoes-container {
    display: flex;
    flex-direction: column;
    max-width: 600px;

    .doacoes-logo {
      width: 150px;
      margin-bottom: 10px;
    }

    .doacoes-titulo {
      font-size: 1.8rem;
      margin-bottom: 10px;

      span {
        color: #d14b4b;
        font-weight: bold;
      }
    }

    .doacoes-descricao {
      font-size: 1rem;
      margin-bottom: 20px;
    }

    .doacoes-botao {
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #d14b4b;
      color: #fff;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      width: 180px;
      height: 50px;
      text-align: center;

      &:hover {
        background-color: #b63939;
      }
    }
  }

  .loja-natalina {
    img {
      width: 500px;
      height: auto;
    }
  }
}

@media (max-width:768px) {
  .natal-doacoes { 
    flex-direction: column;
    align-items: center;
}
.doacoes-container {
  align-items: center;
  text-align: center;
}
.loja-natalina {
  img {
    max-width: 300px;
  }
}
}

@media ( max-width: 480px) {
  .doacoes-container {
    .doacoes-titulo {
      font-size: 1.5rem;
    }
  .doacoes-descricao {
    font-size: 0.8rem;
  }  
  .doacoes-botao {
    font-size: 0.8rem;
    }  
  }
}
</style>
