<template>
  <div class="md:flex md:flex-row border-b-4 border-blue-300 py-6 dark:text-white dark:border-blue-200 transition-colors duration-200">
    <div class="md:basis-1/3">
      <div class="flex justify-center">
        <img class="h-56 rounded-lg" src="../assets/me.png" alt="me" />
      </div>
    </div>
    <div class="md:flex-auto my-2 md:my-auto px-4 text-center md:px-0 md:text-left">
      <h1 class="pb-1 text-2xl font-semibold md:text-4xl">DIEGO ALEJANDRO VARGAS RODRIGUEZ</h1>
      <h2 class="mb-3 text-xl font-semibold">Ingeniero de Sistemas</h2>
      <a href="https://www.linkedin.com/in/diego-vargas-develop/" class="underline hover:font-semibold">
        Linkedin
      </a>
      <br />
      <a href="mailto:dialvaro30@gmail.com" class="underline hover:font-semibold">
        dialvaro30@gmail.com
      </a>
      <br />
      <a href="tel:+573132458975" class="underline hover:font-semibold"> +57 3132458975 </a>
    </div>
    <div class="fixed top-2 ml-2 z-50">
      <ButtonModeDark />
    </div>
  </div>
  <div class="grid border-b-2 border-blue-300 py-5 px-4 sm:px-12 dark:text-white dark:border-blue-200 transition-colors duration-200">
    <h4 class="mb-3 mb-0 mb-2 text-center text-xl font-medium uppercase text-blue-600 dark:text-white dark:underline sm:text-left sm:text-2xl transition-colors duration-200">
      Sobre mí
    </h4>
    <p class="text-justify">
      <b>Soy desarrollador web full stack</b> con más de 4 años de experiencia, en mi corta carrera he
      desarrollado
      diferentes soluciones de software web y desarrollo backend. He estado presente en todo
      el ciclo de vida del desarrollo de software, proporcionando soluciones de TI para
      organizaciones públicas y privadas. <br /><br />
      Me considero una persona pro activa, entusiasta de la tecnología y el aprendizaje, nunca han habido excusas
      para
      aprender algo nuevo.
    </p>
  </div>
</template>
<script setup>
import ButtonModeDark from "../components/ButtonModeDark.vue";
</script>