<template>
  <ul class="ml-1 mt-8 flex items-center">
    <li class="mr-5 text-xs">
      <a
        class="block text-slate-200"
        href="https://www.linkedin.com/in/ernivic-orate-57741a104/"
        target="_blank"
      >
        <span class="sr-only">LinkedIn</span>
        <svg
          viewBox="0 0 24 24"
          fill="currentColor"
          class="h-6 w-6"
          aria-hidden="true"
        >
          <path
            d="M20.5 2h-17A1.5 1.5 0 002 3.5v17A1.5 1.5 0 003.5 22h17a1.5 1.5 0 001.5-1.5v-17A1.5 1.5 0 0020.5 2zM8 19H5v-9h3zM6.5 8.25A1.75 1.75 0 118.3 6.5a1.78 1.78 0 01-1.8 1.75zM19 19h-3v-4.74c0-1.42-.6-1.93-1.38-1.93A1.74 1.74 0 0013 14.19a.66.66 0 000 .14V19h-3v-9h2.9v1.3a3.11 3.11 0 012.7-1.4c1.55 0 3.36.86 3.36 3.66z"
          ></path>
        </svg>
      </a>
    </li>
    <li class="mr-5 text-xs">
      <a class="block text-slate-200" href="mailto:vcui.tan@gmail.com">
        <span class="sr-only">Gmail</span>
        <svg
          width="24px"
          height="24px"
          viewBox="0 0 24 24"
          fill="currentColor"
          stroke="none"
        >
          <g id="SVGRepo_bgCarrier" stroke-width="0" />
          <g
            id="SVGRepo_tracerCarrier"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <g id="SVGRepo_iconCarrier">
            <g>
              <path fill="none" d="M0 0h24v24H0z" />
              <path
                d="M3 3h18a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm9.06 8.683L5.648 6.238 4.353 7.762l7.72 6.555 7.581-6.56-1.308-1.513-6.285 5.439z"
              />
            </g>
          </g>
        </svg>
      </a>
    </li>
  </ul>
</template>
<script>
import { defineComponent, ref } from "vue";
export default defineComponent({
  name: "SocialIcons",
});
</script>
