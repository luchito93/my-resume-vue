<template>
  <h4
    class="mb-4 text-center text-xl font-medium uppercase text-blue-600 md:text-left md:text-2xl dark:text-white dark:underline">
    experiencia profesional
  </h4>
  <ol class="relative border-l border-gray-200 dark:border-gray-700">
    <li class="mb-10 ml-4" v-for="(item, index) in experiences" :key="index">
      <div
        class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700">
      </div>
      <a class="text-xl font-extrabold text-gray-900 dark:text-white flex items-center" :href="item.url">
        <img src="../assets/icon-soho.webp" :alt="item.companyimage" class="mr-3 w-auto h-12"> 
        <div>
          <p>{{ item.company }}</p>
          <p class="text-sm">{{ item.startDate }} {{item.endDate ? `| ${item.endDate}` : '| Actualidad' }}</p>
        </div>
      </a>
      <div class="relative border-l border-gray-200 dark:border-gray-700 mt-3">
        <div class="mb-10 ml-4" v-for="(position, i) in item.positions" :key="i">
          <div
            class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700">
          </div>
          <time class="text-gray-900 dark:text-white">
            <p class="underline text-lg font-bold">{{ position.name }}</p>
            <p class="text-sm no-underline">{{ item.startDate }} {{item.endDate ? `| ${item.endDate}` : '| Actualidad' }}</p>
          </time>
          
          <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
            Get access to over 20+ pages
            including a
            dashboard layout, charts, kanban board, calendar, and pre-order E-commerce & Marketing pages.</p>
        </div>
      </div>

    </li>

    <!-- <div v-if="item.positions.length > 1">
        <div class="relative border-l border-gray-200 dark:border-gray-700">
          <div class="mb-10 ml-4" v-for="(position, index) in item.position" :key="index">
            <div
              class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700">
            </div>
            <time class="text-lg font-semibold text-gray-900 dark:text-white">{{ position.name }}</time>
            <span class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">Get access to over 20+ pages
              including a
              dashboard layout, charts, kanban board, calendar, and pre-order E-commerce & Marketing pages.</span>
            <a href="#"
              class="inline-flex items-center py-2 px-4 text-sm font-medium text-gray-900 bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:outline-none focus:ring-gray-200 focus:text-blue-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700 dark:focus:ring-gray-700">Learn
              more <svg class="ml-2 w-3 h-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd"
                  d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z"
                  clip-rule="evenodd"></path>
              </svg>
            </a>
          </div>
        </div>
      </div> -->
  </ol>
</template>
<script lang="ts">
import experiences from "../utils/experiences.json";
export default {
  data() {
    return {
      experiences: experiences
    }
  }
}
</script>