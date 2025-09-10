<template>
  <div
    class="p-4 rounded-md border border-gray-100 dark:border-gray-800 bg-white dark:bg-gray-900 shadow flex flex-col gap-2">
    <span class="font-semibold text-gray-800 dark:text-gray-200">
      {{ project.title }}
    </span>
    <div class="flex gap-1">
      <Badge v-for="tech in project.techs" :name="tech"></Badge>
    </div>
    <p class="text-sm text-gray-800 dark:text-gray-400">
      {{ project.description }}
    </p>

    <div class="w-full flex justify-center mt-2">
      <button
        @click="showModal = true"
        class="bg-violet-800 text-white font-medium text-sm py-1 px-2 rounded-md cursor-pointer hover:bg-violet-900">
        See more
      </button>
    </div>

    <div
      v-if="showModal"
      @click="showModal = false"
      class="absolute flex items-center justify-center w-screen h-screen dark:bg-gray-500/30 bg-gray-400/40 top-0 left-0">
      <div
        @click="(event) => event.stopPropagation()"
        class="w-full max-w-lg h-fit flex flex-col p-4 rounded-lg bg-white dark:bg-gray-900 dark:border dark:border-gray-800">
        <div class="w-full flex justify-between items-center">
          <span class="font-semibold text-lg text-gray-800 dark:text-gray-200">
            Tasks
          </span>
          <button
            @click="showModal = false"
            class="rounded-md hover:bg-gray-100 dark:hover:bg-gray-800 cursor-pointer">
            <svg
              class="w-7 h-7 fill-gray-800 dark:fill-gray-600"
              viewBox="0 -0.5 25 25"
              xmlns="http://www.w3.org/2000/svg">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier">
                <path
                  d="M6.96967 16.4697C6.67678 16.7626 6.67678 17.2374 6.96967 17.5303C7.26256 17.8232 7.73744 17.8232 8.03033 17.5303L6.96967 16.4697ZM13.0303 12.5303C13.3232 12.2374 13.3232 11.7626 13.0303 11.4697C12.7374 11.1768 12.2626 11.1768 11.9697 11.4697L13.0303 12.5303ZM11.9697 11.4697C11.6768 11.7626 11.6768 12.2374 11.9697 12.5303C12.2626 12.8232 12.7374 12.8232 13.0303 12.5303L11.9697 11.4697ZM18.0303 7.53033C18.3232 7.23744 18.3232 6.76256 18.0303 6.46967C17.7374 6.17678 17.2626 6.17678 16.9697 6.46967L18.0303 7.53033ZM13.0303 11.4697C12.7374 11.1768 12.2626 11.1768 11.9697 11.4697C11.6768 11.7626 11.6768 12.2374 11.9697 12.5303L13.0303 11.4697ZM16.9697 17.5303C17.2626 17.8232 17.7374 17.8232 18.0303 17.5303C18.3232 17.2374 18.3232 16.7626 18.0303 16.4697L16.9697 17.5303ZM11.9697 12.5303C12.2626 12.8232 12.7374 12.8232 13.0303 12.5303C13.3232 12.2374 13.3232 11.7626 13.0303 11.4697L11.9697 12.5303ZM8.03033 6.46967C7.73744 6.17678 7.26256 6.17678 6.96967 6.46967C6.67678 6.76256 6.67678 7.23744 6.96967 7.53033L8.03033 6.46967ZM8.03033 17.5303L13.0303 12.5303L11.9697 11.4697L6.96967 16.4697L8.03033 17.5303ZM13.0303 12.5303L18.0303 7.53033L16.9697 6.46967L11.9697 11.4697L13.0303 12.5303ZM11.9697 12.5303L16.9697 17.5303L18.0303 16.4697L13.0303 11.4697L11.9697 12.5303ZM13.0303 11.4697L8.03033 6.46967L6.96967 7.53033L11.9697 12.5303L13.0303 11.4697Z"></path>
              </g>
            </svg>
          </button>
        </div>
        <div
          class="flex flex-col gap-3 mt-2 text-gray-600 dark:text-gray-500 px-6">
          <div
            class="flex items-center gap-2 w-full"
            v-for="task in project.tasks">
            <svg
              class="w-6 min-w-6 h-6 fill-gray-600 dark:fill-gray-500"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g
                id="SVGRepo_tracerCarrier"
                stroke-linecap="round"
                stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier">
                <path
                  d="M12 9.5C13.3807 9.5 14.5 10.6193 14.5 12C14.5 13.3807 13.3807 14.5 12 14.5C10.6193 14.5 9.5 13.3807 9.5 12C9.5 10.6193 10.6193 9.5 12 9.5Z"></path>
              </g>
            </svg>
            <p class="text-sm">{{ task }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Project } from "#components";

interface Project {
  title: string;
  techs: string[];
  description: string;
  tasks: string[];
  githubLink: string;
}

interface Props {
  project: Project;
}

const props = defineProps<Props>();
const showModal = ref(false);
</script>
