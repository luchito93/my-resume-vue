<template>
  <h4
    class="mb-4 text-center text-xl font-medium uppercase text-blue-600 md:text-left md:text-2xl dark:text-white dark:underline transition-colors duration-200">
    experiencia profesional
  </h4>
  <ol class="relative border-l border-gray-200 dark:border-gray-700 transition-colors duration-200">
    <li class="mb-10 ml-4" v-for="(item, index) in experiences" :key="index">
      <div
        class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700 transition-colors duration-200">
      </div>
      <a class="text-xl font-extrabold text-gray-900 dark:text-white flex items-center transition-colors duration-200" :href="item.url">
        <img :src="item.image" :alt="item.companyimage" class="mr-3 w-12 h-auto rounded-full"> 
        <div>
          <p>{{ item.company }}</p>
          <p class="text-sm">{{ item.startDate }} {{item.endDate ? `a ${item.endDate}` : '| Actualidad' }} {{item.showDate ? ' | ' + calculateTime(item.startDate, item.endDate) : null}}</p>
        </div>
      </a>
      <div class="relative border-l border-gray-200 dark:border-gray-700 mt-3 transition-colors duration-200">
        <div class="mb-2 ml-4" v-for="(position, i) in item.positions" :key="i">
          <div
            class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700 transition-colors duration-200">
          </div>
          <div class="md:flex">
            <div class="md:basis-full">
              <time class="text-gray-900 dark:text-white transition-colors duration-200">
                <p class="underline text-lg font-bold">{{ position.name }}</p>
                <p class="text-sm no-underline" v-if="position.showDate">
                {{ position.startDate }} {{position.endDate ? `a ${position.endDate} |` : '| Actualidad |' }} {{calculateTime(position.startDate, position.endDate)}}
                </p>
              </time>
              <ul class="mb-4 text-base font-normal list-disc	text-gray-500 dark:text-gray-400 ml-4 transition-colors duration-200">
                <li v-for="(responsability, index) in position.responsabilities" :key="index">
                  {{responsability}}
                </li>
              </ul>
            </div>
            <div class="md:basis-1/4 flex flex-wrap items-center hidden">
              <p class="w-full text-center font-bold">Skills</p>
              <span v-for="(skill, index) in position.skills" :key="index" class="bg-blue-100 text-blue-800 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded dark:bg-blue-200 dark:text-blue-800 h-5 mb-2 md:mb-0 transition-colors duration-200">
                {{skill}}
              </span>
            </div>
          </div>
        </div>
      </div>
    </li>
  </ol>
</template>
<script lang="ts">
import dayjs from 'dayjs'
import experiences from "../utils/experiences.json";
export default {
  data() {
    return {
      experiences: experiences
    }
  },
  methods: {
    calculateTime(startDate:string, endDate:string) {
      if (endDate) {
        return dayjs(endDate).diff(startDate, 'month') + ' Meses'
      } else {
        const now = dayjs(new Date).format('YYYY/MM/DD')
        return dayjs(now).diff(startDate, 'month') + ' Meses'
      }      
    }
  }
}
</script>