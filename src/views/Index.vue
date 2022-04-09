<template>
  <div class="relative">
    <div class="container mx-auto bg-white shadow-2xl">
      <div class="grid border-b-4 py-6 sm:grid-flow-col sm:grid-rows-1">
        <div class="row-span-2">
          <div class="flex justify-center">
            <img class="h-56 rounded-lg" src="../assets/me.png" alt="me" />
          </div>
        </div>
        <div class="my-auto px-4 text-center sm:col-span-1 sm:px-0 sm:text-left">
          <h4 class="pb-1 text-2xl font-semibold sm:text-4xl">DIEGO ALEJANDRO VARGAS RODRIGUEZ</h4>
          <h4 class="mb-3 text-xl font-semibold">Ingeniero de Sistemas</h4>
          <a href="https://www.linkedin.com/in/diego-vargas-develop/" class="hover:underline">
            Linkedin
          </a>
          <br />
          <a href="mailto:dialvaro30@gmail.com" class="hover:underline"> dialvaro30@gmail.com </a>
          <br />
          <a href="tel:+573132458975" class="hover:underline"> +57 3132458975 </a>
        </div>
      </div>
      <div class="grid border-b-2 py-5 px-4 sm:px-12">
        <h4
          class="
            mb-3 mb-0 mb-2
            text-center text-xl
            font-medium
            uppercase
            text-sky-600
            sm:text-left sm:text-2xl
          "
        >
          Sobre mí
        </h4>
        <p class="text-justify">
          <b>Desarrollador web full-stack</b> con más de 4 años de experiencia, involucrado en todo
          el ciclo de vida del desarrollo de software, proporcionando soluciones de TI para
          organizaciones públicas y privadas con tecnologías como MySQL, Oracle 11g, PostgreSQL,
          Laravel, Vuejs, Nuxtjs, Digital Ocean, Bootstrap, TailwindCSS y Javascript. <br /><br />
          Me considero un entusiasta de la tecnología y el aprendizaje, nunca ha habido excusas para
          aprender algo nuevo.
        </p>
      </div>
      <div class="flex flex-row px-4 py-5 sm:px-12">
        <div class="basis-3/4">
          <h4
            class="
              mb-3 mb-0 mb-2
              text-center text-xl
              font-medium
              uppercase
              text-sky-600
              sm:text-left sm:text-2xl
            "
          >
            experiencia profesional
          </h4>
        </div>
        <div class="basis-1/4">03</div>
      </div>
    </div>
  </div>
  <!-- <section>
    <div class="container mx-auto py-8 text-center">
      <div>
        <p class="text-10xl font-medium uppercase tracking-wide text-gray-600 dark:text-gray-200">
          Counter:
        </p>
        <h5 class="text-8xl font-bold text-white">
          <span class="inline text-gray-600 dark:text-white">
            {{ appStore.counter.count }}
          </span>
        </h5>
      </div>

      <div class="mx-auto mt-4 flex w-52 p-4">
        <button
          type="button"
          class="
            w-full
            rounded-lg
            bg-white
            py-2
            px-4
            text-center text-base
            font-semibold
            text-indigo-500 text-white
            shadow-md
            transition
            duration-200
            ease-in
            hover:bg-gray-100
            focus:outline-none
            focus:ring-2
            focus:ring-indigo-500
            focus:ring-offset-2
            focus:ring-offset-indigo-200
          "
          @click="appStore.counter.increment()"
        >
          increment
        </button>
      </div>
    </div>
  </section>
  <div class="flex flex-row flex-wrap items-center justify-center gap-4">
        <div>
          <div
            class="
              relative
              mr-2
              inline-block
              w-10
              select-none
              align-middle
              transition
              duration-200
              ease-in
            "
          >
            <input
              id="prefix-1"
              type="checkbox"
              name="toggle"
              :checked="isDark"
              class="
                absolute
                right-4
                block
                h-6
                w-6
                cursor-pointer
                appearance-none
                rounded-full
                border-4
                bg-white
                duration-200
                ease-in
                checked:right-0 checked:bg-blue-600
              "
              @click="toggleDark()"
            /><label
              for="prefix-1"
              class="block h-6 cursor-pointer overflow-hidden rounded-full bg-gray-300"
            ></label>
          </div>
          <span class="font-medium text-gray-600 dark:text-gray-200">Dark mode</span>
        </div>
      </div> -->
  <!-- <Footer /> -->
</template>

<script setup lang="ts">
import appStore from "../store";
import Footer from "../components/Footer.vue";
import { toggleDark } from "../utils/darkMode";
import { isDark } from "../utils/darkMode";
</script>
<style scoped></style>
