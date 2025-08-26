<template>
  <div
    class="bg-gray-200 dark:bg-gray-950 min-h-screen w-screen max-w-screen overflow-hidden px-8 sm:px-4">
    <div
      class="flex flex-col gap-8 justify-start mt-32 sm:mt-40 items-center max-w-4xl mx-auto">
      <div
        class="flex items-center px-4 py-2 text-sm rounded-full text-gray-800 dark:text-gray-300 border border-gray-800 dark:border-gray-300">
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

      <Profile></Profile>

      <span
        class="text-5xl font-semibold text-gray-800 dark:text-gray-100 text-center">
        Software Engineer
      </span>
      <p
        class="text-gray-600 dark:text-gray-400 text-lg text-pretty font-bold tracking-wider text-center">
        Graduating from Mines de Saint-Étienne with a strong interest in
        software craftsmanship and clean architecture. I design scalable,
        maintainable systems through well-structured, reliable code.
      </p>

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
