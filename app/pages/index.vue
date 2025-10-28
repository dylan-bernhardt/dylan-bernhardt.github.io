<template>
  <div
    class="bg-neutral-200 dark:bg-black min-h-screen w-full max-w-screen flex flex-col items-center overflow-hidden px-8 sm:px-4">
    <span class="dark:text-white mt-44 mb-12 text-6xl font-bold">
      Who am I ?
    </span>
    <div
      class="w-full max-w-4xl lg:grid flex flex-row flex-wrap justify-center gap-4 grid-flow-row grid-cols-3 grid-rows-3 bg-neutral-100 dark:bg-neutral-900 lg:p-12 p-8 rounded-4xl">
      <Profile></Profile>
      <div
        class="col-span-2 flex items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <span
          class="text-4xl sm:text-5xl font-extrabold text-neutral-900 dark:text-neutral-100 text-center">
          Software Engineer
        </span>
      </div>

      <div
        class="col-span-2 flex items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
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
        class="row-span-2 flex items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <p class="text-neutral-500 dark:text-neutral-300 text-base">
          Graduating from Mines de Saint-Étienne with a strong interest in
          software craftsmanship and clean architecture. I design scalable,
          maintainable systems through well-structured, reliable code.
        </p>
      </div>

      <div
        class="col-span-2 flex flex-col sm:flex-row gap-2 sm:gap-8 items-center justify-center bg-linear-to-br from-white to-neutral-100 dark:from-neutral-800 dark:to-neutral-900 p-8 rounded-3xl dark:inset-shadow-sm dark:inset-shadow-neutral-700 shadow-md dark:shadow-neutral-950">
        <span
          class="text-2xl font-extrabold text-neutral-400 dark:text-neutral-500 text-center">
          Want more info ?
        </span>

        <a href="./cv.pdf" target="_blank">
          <button
            class="group relative inline-flex h-12 items-center justify-center overflow-hidden rounded-md bg-neutral-950 dark:bg-neutral-100 px-6 font-medium text-neutral-200 dark:text-neutral-900 duration-500 cursor-pointer">
            <div
              class="translate-x-0 opacity-100 transition group-hover:-translate-x-[150%] group-hover:opacity-0">
              Download Resume
            </div>
            <div
              class="absolute translate-x-[150%] opacity-0 transition group-hover:translate-x-0 group-hover:opacity-100">
              <svg
                viewBox="0 0 24 24"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
                class="h-6 w-6">
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g
                  id="SVGRepo_tracerCarrier"
                  stroke-linecap="round"
                  stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <path
                    d="M5.625 15C5.625 14.5858 5.28921 14.25 4.875 14.25C4.46079 14.25 4.125 14.5858 4.125 15H5.625ZM4.875 16H4.125H4.875ZM19.275 15C19.275 14.5858 18.9392 14.25 18.525 14.25C18.1108 14.25 17.775 14.5858 17.775 15H19.275ZM11.1086 15.5387C10.8539 15.8653 10.9121 16.3366 11.2387 16.5914C11.5653 16.8461 12.0366 16.7879 12.2914 16.4613L11.1086 15.5387ZM16.1914 11.4613C16.4461 11.1347 16.3879 10.6634 16.0613 10.4086C15.7347 10.1539 15.2634 10.2121 15.0086 10.5387L16.1914 11.4613ZM11.1086 16.4613C11.3634 16.7879 11.8347 16.8461 12.1613 16.5914C12.4879 16.3366 12.5461 15.8653 12.2914 15.5387L11.1086 16.4613ZM8.39138 10.5387C8.13662 10.2121 7.66533 10.1539 7.33873 10.4086C7.01212 10.6634 6.95387 11.1347 7.20862 11.4613L8.39138 10.5387ZM10.95 16C10.95 16.4142 11.2858 16.75 11.7 16.75C12.1142 16.75 12.45 16.4142 12.45 16H10.95ZM12.45 5C12.45 4.58579 12.1142 4.25 11.7 4.25C11.2858 4.25 10.95 4.58579 10.95 5H12.45ZM4.125 15V16H5.625V15H4.125ZM4.125 16C4.125 18.0531 5.75257 19.75 7.8 19.75V18.25C6.61657 18.25 5.625 17.2607 5.625 16H4.125ZM7.8 19.75H15.6V18.25H7.8V19.75ZM15.6 19.75C17.6474 19.75 19.275 18.0531 19.275 16H17.775C17.775 17.2607 16.7834 18.25 15.6 18.25V19.75ZM19.275 16V15H17.775V16H19.275ZM12.2914 16.4613L16.1914 11.4613L15.0086 10.5387L11.1086 15.5387L12.2914 16.4613ZM12.2914 15.5387L8.39138 10.5387L7.20862 11.4613L11.1086 16.4613L12.2914 15.5387ZM12.45 16V5H10.95V16H12.45Z"></path>
                </g>
              </svg>
            </div>
          </button>
        </a>
      </div>
    </div>

    <span class="dark:text-white mt-32 mb-12 text-6xl font-bold text-center">
      Wanna see some projects ?
    </span>

    <NuxtLink to="projects" class="mb-12">
      <button
        class="group relative inline-flex h-12 items-center justify-center overflow-hidden rounded-md bg-neutral-950 px-6 font-medium text-neutral-200 duration-500 cursor-pointer">
        <div
          class="text-xl translate-x-0 opacity-100 transition group-hover:-translate-x-[150%] group-hover:opacity-0">
          Yeah go !
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
    </NuxtLink>
  </div>
</template>
