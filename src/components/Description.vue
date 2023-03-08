<template>
  <div
    class="border-b-4 border-blue-300 py-6 transition-colors duration-200 dark:border-blue-200 dark:text-white md:flex md:flex-row"
  >
    <div class="md:basis-1/3">
      <div class="flex justify-center">
        <img class="h-56 rounded-lg" src="../assets/me.png" alt="me" />
      </div>
    </div>
    <div class="my-2 px-4 text-center md:my-auto md:flex-auto md:px-0 md:text-left">
      <h1 class="pb-1 text-2xl font-semibold md:text-4xl">DIEGO ALEJANDRO VARGAS RODRIGUEZ</h1>
      <h2 class="mb-3 text-xl font-semibold">Ingeniero de Sistemas</h2>
      <a
        href="https://www.linkedin.com/in/diego-vargas-develop/"
        class="underline hover:font-semibold"
      >
        Linkedin
      </a>
      <br />
      <a href="mailto:dialvaro30@gmail.com" class="underline hover:font-semibold">
        dialvaro30@gmail.com
      </a>
      <br />
      <a href="tel:+573132458975" class="underline hover:font-semibold"> +57 3132458975 </a>
    </div>
    <div class="fixed top-2 z-50 ml-2">
      <ButtonModeDark />
    </div>
  </div>
  <div
    class="grid border-b-2 border-blue-300 py-5 px-4 transition-colors duration-200 dark:border-blue-200 dark:text-white sm:px-12"
  >
    <h4
      class="mb-3 mb-0 mb-2 text-center text-xl font-medium uppercase text-blue-600 transition-colors duration-200 dark:text-white dark:underline sm:text-left sm:text-2xl"
    >
      Sobre mí
    </h4>
    <p class="text-justify">
      <b>Soy desarrollador web full stack</b> con más de 4 años de experiencia, en mi carrera he
      analizado, diseñado e implementado diferentes soluciones de software web y desarrollo backend.
      He estado presente en todo el ciclo de vida del desarrollo de software, proporcionando
      soluciones de TI para organizaciones públicas y privadas. <br /><br />
      Me considero una persona pro activa, compañerista, paciente, confiable, entusiasta de la
      tecnología y el aprendizaje, nunca han habido excusas para aprender algo nuevo.
    </p>
  </div>
</template>
<script setup>
import ButtonModeDark from "../components/ButtonModeDark.vue";
</script>
