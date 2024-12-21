<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import presentes from "../assets/presentes.png";

const targetDate = new Date(new Date().getFullYear(), 11, 25);
const timeRemaining = ref(null);
let timer = null;

const updateTimer = () => {
  const now = new Date();
  const difference = targetDate - now;

  if (difference <= 0) {
    clearInterval(timer);
    timeRemaining.value = null;
    return;
  }

  const days = Math.floor(difference / (1000 * 60 * 60 * 24));
  const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((difference % (1000 * 60)) / 1000);

  timeRemaining.value = { days, hours, minutes, seconds };
};

onMounted(() => {
  updateTimer();
  timer = setInterval(updateTimer, 1000);
});

onBeforeUnmount(() => {
  clearInterval(timer);
});
</script>

<template>
  <!--Insira as tags-->
  <section>
    <div>
      <h1>Tempo limitado</h1>
      <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
    </div>
    <div class="cronometro">
      <p v-if="timeRemaining">
        {{ timeRemaining.days }} d-
        {{ timeRemaining.hours }} h-
        {{ timeRemaining.minutes }} m-
        {{ timeRemaining.seconds }} s
      </p>
      <p v-else>Feliz Natal!! 🎄</p>
    </div>
    <img :src="presentes" alt="imagem de presentes">
  </section>
</template>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,100..900;1,100..900&display=swap');


section {
  font-family: "Archivo", sans-serif;
  padding: 20px 25px;
  background: #F9F9F9;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  div {
    margin: 20px;
    width: 40vw;
    height: 27vh;
    flex-wrap: wrap;
    padding: 40px 20px;
  }
}

.cronometro {
  width: 50vw;
  height: 15vh;
  font-family: "Archivo", sans-serif;
  margin-top: 0;
  margin-bottom: 25px;
  p {
    margin-top: 0;
    color: #CD3C32;
    font-weight: 600;
    font-size: 64px;
    text-align: center;
  }

}

h1 {
  font-weight: 600;
  font-size: 40px;
  text-align: center;
  line-height: 0.5;
}

p {
  font-weight: 400;
  font-size: 20px;
  color: #121214;
  text-align: center;
}
</style>