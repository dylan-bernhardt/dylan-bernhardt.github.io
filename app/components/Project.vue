<template>
  <div
    class="w-full max-w-4xl grid gap-4 grid-cols-3 bg-neutral-100 dark:bg-neutral-900 p-12 rounded-4xl">
    <div
      class="col-span-3 flex items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
      <span
        class="text-2xl font-extrabold text-neutral-900 dark:text-neutral-100 text-center">
        {{ project.title }}
      </span>
    </div>

    <div
      class="col-span-2 flex items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
      <p class="text-neutral-500 dark:text-neutral-300 text-base">
        {{ project.description }}
      </p>
    </div>

    <div
      class="flex flex-col gap-2 bg-linear-to-bl from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950 overflow-hidden">
      <img
        class="w-full h-auto object-cover"
        :src="project.image"
        ></img>
    </div>

    <div
      class="flex flex-wrap gap-2 items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-4 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
      <Badge v-for="tech in project.techs" :name="tech"></Badge>
    </div>

    <div
      class="col-span-2 flex gap-4 items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
      <span
        class="text-2xl font-extrabold text-neutral-400 dark:text-neutral-500 text-center">
        Want more info ?
      </span>

      <button
        @click="showModal = true"
        class="group relative flex h-12 items-center justify-center overflow-hidden rounded-md bg-neutral-950 dark:bg-neutral-100 px-6 font-medium text-neutral-200 dark:text-neutral-900 duration-500 cursor-pointer">
        <div
          class="translate-x-0 opacity-100 transition group-hover:-translate-x-[150%] group-hover:opacity-0">
          Show details
        </div>
        <div
          class="absolute translate-x-[150%] opacity-0 transition group-hover:translate-x-0 group-hover:opacity-100">
          <svg
            width="15"
            height="15"
            viewBox="0 0 15 15"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6">
            <path
              d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z"
              fill="currentColor"
              fill-rule="evenodd"
              clip-rule="evenodd"></path>
          </svg>
        </div>
      </button>

      <NuxtLink
        v-if="project.githubLink !== ''"
        :to="project.githubLink"
        target="_blank">
        <button
          v-if="project.githubLink !== ''"
          class="flex items-center justify-center rounded-md bg-neutral-950 dark:bg-neutral-100 p-1 h-12 w-12 cursor-pointer">
          <svg
            class="w-5 h-5 fill-neutral-200 dark:fill-neutral-900"
            viewBox="0 0 32 32"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg">
            <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
            <g
              id="SVGRepo_tracerCarrier"
              stroke-linecap="round"
              stroke-linejoin="round"></g>
            <g id="SVGRepo_iconCarrier">
              <title>github</title>
              <path
                d="M16 1.375c-8.282 0-14.996 6.714-14.996 14.996 0 6.585 4.245 12.18 10.148 14.195l0.106 0.031c0.75 0.141 1.025-0.322 1.025-0.721 0-0.356-0.012-1.3-0.019-2.549-4.171 0.905-5.051-2.012-5.051-2.012-0.288-0.925-0.878-1.685-1.653-2.184l-0.016-0.009c-1.358-0.93 0.105-0.911 0.105-0.911 0.987 0.139 1.814 0.718 2.289 1.53l0.008 0.015c0.554 0.995 1.6 1.657 2.801 1.657 0.576 0 1.116-0.152 1.582-0.419l-0.016 0.008c0.072-0.791 0.421-1.489 0.949-2.005l0.001-0.001c-3.33-0.375-6.831-1.665-6.831-7.41-0-0.027-0.001-0.058-0.001-0.089 0-1.521 0.587-2.905 1.547-3.938l-0.003 0.004c-0.203-0.542-0.321-1.168-0.321-1.821 0-0.777 0.166-1.516 0.465-2.182l-0.014 0.034s1.256-0.402 4.124 1.537c1.124-0.321 2.415-0.506 3.749-0.506s2.625 0.185 3.849 0.53l-0.1-0.024c2.849-1.939 4.105-1.537 4.105-1.537 0.285 0.642 0.451 1.39 0.451 2.177 0 0.642-0.11 1.258-0.313 1.83l0.012-0.038c0.953 1.032 1.538 2.416 1.538 3.937 0 0.031-0 0.061-0.001 0.091l0-0.005c0 5.761-3.505 7.029-6.842 7.398 0.632 0.647 1.022 1.532 1.022 2.509 0 0.093-0.004 0.186-0.011 0.278l0.001-0.012c0 2.007-0.019 3.619-0.019 4.106 0 0.394 0.262 0.862 1.031 0.712 6.028-2.029 10.292-7.629 10.292-14.226 0-8.272-6.706-14.977-14.977-14.977-0.006 0-0.013 0-0.019 0h0.001z"></path>
            </g>
          </svg>
        </button>
      </NuxtLink>
    </div>
  </div>

  <div
    v-if="showModal"
    @click="showModal = false"
    class="z-50 fixed flex items-center justify-center w-screen h-screen dark:bg-neutral-900/50 backdrop-blur-lg bg-neutral-300/50 top-0 left-0">
    <div
      @click="(event) => event.stopPropagation()"
      class="w-full max-w-lg h-fit flex flex-col p-6 rounded-xl bg-white dark:bg-gray-900 dark:border dark:border-gray-800">
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
</template>

<script setup lang="ts">
import { Project } from "#components";

interface Project {
  title: string;
  techs: string[];
  description: string;
  tasks: string[];
  githubLink: string;
  image: string;
}

interface Props {
  project: Project;
}

const props = defineProps<Props>();
const showModal = ref(false);
</script>
