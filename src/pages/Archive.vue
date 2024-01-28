<template>
  <div id="arhive-page">
    <div class="main-container max-w-screen-xl min-h-screen mx-auto px-24">
      <div class="py-24">
        <a
          class="group mb-2 inline-flex items-center font-semibold leading-tight text-teal-300"
          href="/"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            class="mr-1 h-4 w-4 rotate-180 transition-transform group-hover:-translate-x-2"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M3 10a.75.75 0 01.75-.75h10.638L10.23 5.29a.75.75 0 111.04-1.08l5.5 5.25a.75.75 0 010 1.08l-5.5 5.25a.75.75 0 11-1.04-1.08l4.158-3.96H3.75A.75.75 0 013 10z"
              clip-rule="evenodd"
            ></path>
          </svg>
          Ernivic Orate
        </a>
        <h1 class="text-4xl font-bold tracking-tight text-slate-200 text-5xl">
          All Projects
        </h1>
        <table
          id="content"
          class="mt-12 w-full border-collapse text-left text-slate-400"
        >
          <thead
            class="sticky top-0 z-10 border-b border-slate-300/10 bg-slate-900/75 px-6 py-5 backdrop-blur"
          >
            <tr>
              <th class="py-4 pr-8 text-sm font-semibold text-slate-200">
                Year
              </th>
              <th class="py-4 pr-8 text-sm font-semibold text-slate-200">
                Project
              </th>
              <th class="py-4 pr-8 text-sm font-semibold text-slate-200"></th>
              <th class="py-4 pr-8 text-sm font-semibold text-slate-200">
                Built with
              </th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="projects in proj"
              :key="projects.title"
              class="border-b border-slate-300 last:border-none"
            >
              <td class="py-4 pr-4 align-top text-sm">
                <div class="translate-y-px">{{ projects.year }}</div>
              </td>
              <td
                class="py-4 pr-4 align-top font-semibold leading-snug text-slate-200"
              >
                <a
                  style="color: #ffffffbf"
                  :href="projects.url"
                  target="_blank"
                  rel="noreferrer noopener"
                  >{{ projects.title }}</a
                >
              </td>
              <td class="py-4 pr-4 align-top text-sm">
                {{ projects.titlesub }}
              </td>
              <td class="py-4 pr-4 align-top text-sm">
                <ul
                  class="flex -translate-y-1.5 flex-wrap"
                  aria-label="Technologies used"
                >
                  <li
                    class="my-1 mr-1.5"
                    v-for="techno in projects.tech"
                    :key="techno"
                    style="margin-top: 3px; margin-bottom: 3px"
                  >
                    <div
                      class="flex items-center rounded-full bg-teal-400 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                    >
                      {{ techno }}
                    </div>
                  </li>
                </ul>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { proj } from "../utils/projects";

export default defineComponent({
  name: "ArchivePage",

  setup() {
    return {
      proj,
    };
  },
});
</script>
