<template>
  <div
    class="bg-neutral-200 dark:bg-black h-screen w-screen max-w-screen flex flex-col items-center overflow-hidden px-8 sm:px-4">
    <span class="dark:text-white mt-44 mb-12 text-6xl font-bold">
      Who am I ?
    </span>
    <div
      class="w-full max-w-4xl grid gap-4 grid-flow-row grid-cols-3 grid-rows-3 bg-neutral-100 dark:bg-neutral-900 p-12 rounded-4xl">
      <Profile></Profile>
      <div
        class="col-span-2 flex items-center justify-center bg-white dark:bg-neutral-800 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <span
          class="text-5xl font-extrabold text-neutral-900 dark:text-neutral-100 text-center">
          Software Engineer
        </span>
      </div>

      <div
        class="col-span-2 flex items-center justify-center bg-white dark:bg-neutral-800 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <div
          class="flex items-center px-4 py-2 text-sm rounded-lg text-neutral-600 dark:text-neutral-300 bg-neutral-100 dark:bg-neutral-700">
          <svg
            class="shrink-0 inline w-5 h-5 me-4"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="currentColor"
            viewBox="0 0 20 20">
            <path
              d="M10 .5a9.5 9.5 0 1 0 9.5 9.5A9.51 9.51 0 0 0 10 .5ZM9.5 4a1.5 1.5 0 1 1 0 3 1.5 1.5 0 0 1 0-3ZM12 15H8a1 1 0 0 1 0-2h1v-3H8a1 1 0 0 1 0-2h2a1 1 0 0 1 1 1v4h1a1 1 0 0 1 0 2Z" />
          </svg>
          <span class="text-center text-lg">
            Actively seeking a software engineer role !
          </span>
        </div>
      </div>

      <div
        class="row-span-2 flex items-center justify-center bg-white dark:bg-neutral-800 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <p class="text-neutral-500 dark:text-neutral-300 text-base">
          Graduating from Mines de Saint-Étienne with a strong interest in
          software craftsmanship and clean architecture. I design scalable,
          maintainable systems through well-structured, reliable code.
        </p>
      </div>

      <div
        class="col-span-2 flex gap-8 items-center justify-center bg-white dark:bg-neutral-800 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <span
          class="text-2xl font-extrabold text-neutral-400 dark:text-neutral-500 text-center">
          Want more info ?
        </span>

        <a href="./cv.pdf" target="_blank">
          <button
            class="w-full rounded-full flex px-6 py-2 bg-black dark:bg-white text-neutral-100 dark:text-neutral-900 cursor-pointer shadow-md shadow-neutral-300 dark:shadow-neutral-950 text-nowrap">
            Download resume
          </button>
        </a>
      </div>
    </div>
  </div>
</template>
