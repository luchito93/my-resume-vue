<template>
  <h4
    class="mb-4 text-center text-xl font-medium uppercase text-blue-600 transition-colors duration-200 dark:text-white dark:underline md:text-left md:text-2xl"
  >
    experiencia profesional
  </h4>
  <ol class="relative border-l border-gray-200 transition-colors duration-200 dark:border-gray-700">
    <template v-for="item in experiences" :key="item.company + 'it'">
      <li v-if="item.company != 'Raptor Cx'" class="mb-10 ml-4">
        <div
          class="absolute -left-1.5 mt-1.5 h-3 w-3 rounded-full border border-white bg-gray-200 transition-colors duration-200 dark:border-gray-900 dark:bg-gray-700"
        ></div>
        <a
          class="flex items-center text-xl font-extrabold text-gray-900 transition-colors duration-200 dark:text-white"
          :href="item.url"
        >
          <img :src="item.image" :alt="item.company" class="mr-3 h-auto w-12 rounded-full" />
          <div>
            <p>{{ item.company }}</p>
            <p class="text-sm">
              {{ item.startDate }} {{ item.endDate ? `a ${item.endDate}` : "| Actualidad" }}
              {{ item.showDate ? " | " + calculateTime(item.startDate, item.endDate) : null }}
            </p>
          </div>
        </a>
        <div
          class="relative mt-3 border-l border-gray-200 transition-colors duration-200 dark:border-gray-700"
        >
          <template v-for="position in item.positions" :key="position + 'po'">
            <div class="mb-2 ml-4 mr-3">
              <div
                class="absolute -left-1.5 mt-1.5 h-3 w-3 rounded-full border border-white bg-gray-200 transition-colors duration-200 dark:border-gray-900 dark:bg-gray-700"
              ></div>
              <div class="md:flex">
                <div class="md:basis-full">
                  <time class="text-gray-900 transition-colors duration-200 dark:text-white">
                    <p class="text-lg font-bold underline">{{ position.name }}</p>
                    <p v-if="position.showDate" class="text-sm no-underline">
                      {{ position.startDate }}
                      {{ position.endDate ? `a ${position.endDate} |` : "| Actualidad |" }}
                      {{ calculateTime(position.startDate, position.endDate) }}
                    </p>
                  </time>
                  <ul
                    class="mb-4 ml-4 list-disc text-base font-normal text-gray-500 transition-colors duration-200 dark:text-gray-400"
                  >
                    <li v-for="(responsability, index) in position.responsabilities" :key="index">
                      {{ responsability }}
                    </li>
                  </ul>
                  <div class="flex flex-wrap items-center md:basis-1/4">
                    <p class="w-full font-bold underline">Habilidades</p>
                    <span
                      v-for="(skill, index) in position.skills"
                      :key="index"
                      class="mr-2 mb-2 h-5 rounded bg-blue-100 px-2.5 py-0.5 text-xs font-semibold text-blue-800 transition-colors duration-200 dark:bg-blue-200 dark:text-blue-800"
                    >
                      {{ skill }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </template>
        </div>
      </li>
    </template>
  </ol>
</template>
<script lang="ts">
import dayjs from "dayjs";
import experiences from "../utils/experiences.json";
export default {
  data() {
    return {
      experiences: experiences,
    };
  },
  methods: {
    calculateTime(startDate: string, endDate: any) {
      if (endDate) {
        return dayjs(endDate).diff(startDate, "month") + " Meses";
      }
      const now = dayjs(new Date()).format("YYYY/MM/DD");
      return dayjs(now).diff(startDate, "month") + " Meses";
    },
  },
};
</script>
