<script setup>
import logo from "../assets/logo.png"
import twitter from "../assets/twitter.png"
import whatsapp from "../assets/whatsapp.png"
import instagram from "../assets/instagram.png"
import facebook from "../assets/facebook.png"
import google from "../assets/google.png"
</script>

<template>
  <!--Insira as tags-->
  <section>
    <img class="feliz" :src="logo" alt="Feliz Natal">
    <div>
      <img :src="twitter" alt="logo Twitter">
      <img :src="whatsapp" alt="Logo whatsapp">
      <img :src="instagram" alt="logo Instagram">
      <img :src="facebook" alt="logo Facebook">
      <img :src="google" alt="logo Google">
    </div>
  </section>
</template>

<style scoped lang="scss">
  section{
    background: #FFE9E8;
    display: flex;
    width: 100%;
    height: auto;
    margin: -10px -8px;
    padding: 7px;
  }
  .feliz{
    object-fit: fill;
    padding: 10px;
    margin-left: 60px;
  }
  div{
    display: flex;
    width: 420px;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    margin-left: 490px;
    padding: 5px; 
  }
  
</style>