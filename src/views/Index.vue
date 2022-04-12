<template>
  <div class="relative">
    <div class="container mx-auto bg-white shadow-2xl">
      <Description />
      <div class="md:flex md:flex-row px-4 py-5 md:px-12">
        <div class="md:basis-3/4">
          <h4 class="mb-2 text-center text-xl font-medium uppercase text-blue-600 md:text-left md:text-2xl">
            experiencia profesional
          </h4>
        </div>
        <div class="md:flex-auto">
          <Skills />
        </div>
      </div>
    </div>
    <Footer />
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
  <!-- -->
</template>

<script setup lang="ts">
import Description from "../components/Description.vue";
import Skills from "../components/Skills.vue";
import Footer from "../components/Footer.vue";
/* import appStore from "../store";
import { toggleDark } from "../utils/darkMode";
import { isDark } from "../utils/darkMode"; */
</script>
<style scoped>
</style>
