<template>
  <div
    class="bg-gray-300 dark:bg-gray-950 min-h-screen w-screen max-w-screen overflow-hidden px-8 sm:px-4">
    <div
      class="flex flex-col gap-8 justify-start mt-40 sm:mt-64 items-center max-w-4xl mx-auto">
      <div
        class="flex items-center mb-12 px-4 py-2 text-sm rounded-full text-gray-800 dark:text-gray-300 border border-gray-800 dark:border-gray-300">
        <svg
          class="shrink-0 inline w-4 h-4 me-3"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="currentColor"
          viewBox="0 0 20 20">
          <path
            d="M10 .5a9.5 9.5 0 1 0 9.5 9.5A9.51 9.51 0 0 0 10 .5ZM9.5 4a1.5 1.5 0 1 1 0 3 1.5 1.5 0 0 1 0-3ZM12 15H8a1 1 0 0 1 0-2h1v-3H8a1 1 0 0 1 0-2h2a1 1 0 0 1 1 1v4h1a1 1 0 0 1 0 2Z" />
        </svg>
        <span class="text-center">
          Actively seeking a software engineer role starting November 2025.
        </span>
      </div>
      <span
        class="text-5xl font-semibold text-gray-600 dark:text-gray-100 text-center">
        Hello, I'm Dylan
      </span>
      <p
        class="dark:text-gray-400 text-lg text-pretty font-bold tracking-wider text-center">
        Future software engineer graduating from Mines de Saint-Étienne. I care
        about software craftsmanship and build maintainable, scalable systems
        with clean, reliable code.
      </p>
      <div class="flex items-center gap-2 mt-12">
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

        <span
          class="text-sm font-semibold tracking-wider text-gray-600 dark:text-gray-400">
          Strasbourg
        </span>
      </div>

      <div class="flex gap-2 flex-row">
        <a href="./cv.pdf" target="_blank">
          <button
            class="w-full rounded-md flex px-4 py-2 bg-indigo-400 text-white hover:bg-indigo-500 cursor-pointer shadow text-nowrap">
            My resume
          </button>
        </a>
        <div>
          <nuxt-link to="/">
            <button
              class="w-full rounded-md flex px-4 py-2 text-gray-200 bg-gray-400 dark:bg-gray-600 hover:bg-gray-500 dark:hover:bg-gray-800 cursor-pointer shadow text-nowrap">
              My projects
            </button>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>
