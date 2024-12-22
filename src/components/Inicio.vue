<script setup>
import logo from "../assets/logo.png";
import lojaNatalina from "../assets/lojaNatalina.png";

</script>

<template>
<!--Insira as tags-->
<section>
  <div>
    <img :src="logo" alt="">
  <h1>Uma <span> plataforma de doação</span>
    para espalhar alegria</h1>
    <p>Nessas festas de fim de ano mande um presente
      para a pessoa amada e compartilhe a alegria do Natal.</p>
      <button>FAZER UMA DOAÇÃO</button>
  </div>
  <img :src="lojaNatalina" alt="">
    </section>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,100..900;1,100..900&display=swap');


section{
  font-family: "Archivo", sans-serif;
  padding: 60px 55px;
  background: #FFE9E8;
  display: flex;
  align-items: center;
  justify-content: center;
  div{
    margin: 40px;
  }
}

h1{
  font-weight: 600;
  font-size: 40px;
  span{
    color: #CD3C32;
  }
}
p{
  font-weight: 400;
  font-size: 24px;
  color: #121214;
}
button{
  background: #CD3C32;
  color: #FFFFFF;
  padding: 14px 32px;
  gap: 8px;
  border-radius: 2px;
  border-style: none;

}

</style>
