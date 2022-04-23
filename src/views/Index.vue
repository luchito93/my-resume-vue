<template>
  <div class="relative">
    <div class="container mx-auto bg-white shadow-2xl dark:bg-gray-800 transition-colors duration-400">
      <Description />
      <div class="md:flex md:flex-row px-4 py-5 md:px-12">
        <div class="md:basis-3/4">
          <Experiences />
        </div>
        <div class="md:flex-auto">
          <Skills />
          <Education />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Description from "../components/Description.vue";
import Experiences from "../components/Experiences.vue";
import Skills from "../components/Skills.vue";
import Education from "../components/Education.vue";
import Footer from "../components/Footer.vue";
/* import appStore from "../store"; */
</script>