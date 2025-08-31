<template>
  <div class="flex flex-col gap-2 items-center">
    <div
      class="rounded-full overflow-hidden w-20 h-20 flex items-center justify-center">
      <NuxtImg class="w-full h-full" src="./me.jpg" alt="" />
    </div>
    <span class="text-gray-800 dark:text-gray-100 font-semibold text-xl mt-4">
      Hi, I'm Dylan
    </span>

    <div class="flex items-center gap-2">
      <svg
        class="w-5 h-5 fill-gray-600 dark:fill-gray-400"
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

      <span class="text-base font-medium text-gray-600 dark:text-gray-400">
        Strasbourg
      </span>
    </div>
  </div>
</template>
