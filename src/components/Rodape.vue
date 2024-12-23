<script setup>
import logonatal from "../assets/logonatal.png";
import twitter from "../assets/twitter.png";
import whatsapp from "../assets/whatsapp.png";
import instagram from "../assets/instagram.png";
import facebook from "../assets/facebook.png";
import google from "../assets/google.png";
</script>

<template>
  <section class="container-natal">
  <div class="logo-natal">
  <img :src="logonatal" alt="Logo da loja de Natal" >
</div>
<div class="logo-twitter">
  <img :src="twitter" alt="Ícone do Twitter" > 
</div>
<div class="logo-whatsapp">
  <img :src="whatsapp" alt="Ícone do Whatsapp" >
</div>
<div class="logo-instagram">
  <img :src="instagram" alt="Ícone do Instagram" >
  </div>
  <div class="logo-facebook">
  <img :src="facebook" alt="Ícone do Facebook" >
</div>
<div class="logo-google">
  <img :src="google" alt="Ícone do Google" > 
  </div>
</section>
</template>
<style scoped lang="scss">

.container-natal{
  display: flex;
  flex-wrap: wrap;
  justify-content:center;
  align-items: center;
  padding: 5px;
  background-color: #ffe9e8;
}
.logo-natal{
  flex: 1 1 100px;
  display:flex;
  justify-content: space-between; 
  flex-wrap:wrap;
  align-items: center;
  padding: 5px;   
  margin-right: 1rem; 
 

  img {
    max-width: 80%;
    height: auto;
  }
}
 

.logo-twitter{
  margin-bottom: 1rem;
  text-align: center;
  img {
    max-width: 150%;
    height: auto;
  }}

  .logo-whatsapp{
  display: flex;
    margin-bottom: 1rem;  
    text-align: center;
   
    img {
      max-width: 100%;
      height: auto;
    }}

    .logo-instagram{
      margin-bottom: 1rem;
      text-align: center;  
      

      img {
        max-width: 100%;
        height: auto;
      }}

      .logo-facebook{
        margin-bottom: 1rem;
        text-align: center;  

        img {
          max-width: 100%;
          height: auto;
        }}

        .logo-google{
          display: flex;
          margin-bottom: 1rem;
          
          img {
            max-width: 100%;
            height: auto;
          }
        }
</style>