<script setup>
import bola from "../assets/bola.png"
</script>

<template>
<!--Insira as tags-->
<section>
  <img :src="bola" alt="">
  <div> 
  <h1>Conectando generosidade
    ao redor do mundos</h1>
    <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
      <button>FAZER UMA DOAÇÃO</button>
  </div>
  
    </section>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,100..900;1,100..900&display=swap');


section{
  width: 90vw;
  font-family: "Archivo", sans-serif;
  padding: 60px 55px;
  background: #F9F9F9;
  display: flex;
  align-items: center;
  justify-content: center;
 
}
img{
  padding: 20px;
  margin-left: 200px;
}
div{
    margin:160px;
    padding: 20px;
  }

h1{
  width: 38vw;
  font-weight: 600;
  font-size: 40px;
  span{
    color: #CD3C32;
  }
}
p{
  display: flex;
  font-weight: 400;
  font-size: 20px;
  line-height: 30px;
  text-align: justify;
  color: #121214;
  width: 35vw;
  height: 30vh;
}
button{
  background: #CD3C32;
  color: #FFFFFF;
  padding: 14px 32px;
  gap: 8px;
  border-radius: 2px;
  border-style: none;
  margin-top: 0;
}

</style>