<template>
  <div
    class="flex flex-row gap-6 items-center bg-white dark:bg-neutral-800 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
    <div
      class="rounded-full overflow-hidden w-16 h-16 flex items-center justify-center">
      <NuxtImg class="w-full h-full" src="./me.jpg" alt="" />
    </div>
    <div class="flex flex-col gap-0.5 items-center justify-center">
      <p>
        <span class="text-neutral-400 dark:text-neutral-500 text-lg mt-4">
          Hi, I'm
        </span>

        <span
          class="text-neutral-900 dark:text-neutral-100 text-lg font-semibold mt-4">
          Dylan
        </span>
      </p>

      <div class="flex items-center gap-2">
        <svg
          class="w-4 h-4 fill-neutral-500 dark:fill-neutral-300"
          height="200px"
          width="200px"
          version="1.1"
          id="Filled_Icons"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px"
          y="0px"
          viewBox="0 0 24 24"
          enable-background="new 0 0 24 24"
          xml:space="preserve">
          <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
          <g
            id="SVGRepo_tracerCarrier"
            stroke-linecap="round"
            stroke-linejoin="round"></g>
          <g id="SVGRepo_iconCarrier">
            <g id="Location-Pin-Filled">
              <path
                d="M12,1c-4.97,0-9,4.03-9,9c0,6.75,9,13,9,13s9-6.25,9-13C21,5.03,16.97,1,12,1z M12,13c-1.66,0-3-1.34-3-3s1.34-3,3-3 s3,1.34,3,3S13.66,13,12,13z"></path>
            </g>
          </g>
        </svg>

        <span class="text-base text-neutral-500 dark:text-neutral-300">
          Strasbourg
        </span>
      </div>
    </div>
  </div>
</template>
