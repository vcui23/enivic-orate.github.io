<template>
  <section id="projects">
    <div class="scroll-section mb-36 scroll-mt-24">
      <ul>
        <li class="mb-12" v-for="projects in proj.slice(0, 5)" :key="projects.title">
          <div
            class="proj-sec group relative grid grid-cols-8 gap-4 pb-1 transition-all gap-4 opacity-100 opacity-50"
          >
            <div
              class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none -inset-x-6 block bg-slate-800 drop-shadow-lg"
            ></div>
            <div class="z-10 order-2 col-span-6">
              <h3>
                <a
                  class="inline-flex items-baseline font-medium leading-tight text-slate-200 text-base"
                  :href="projects.url"
                  target="_blank"
                  rel="noreferrer"
                  :aria-label="projects.title"
                >
                  <span
                    class="absolute -inset-x-4 -inset-y-2.5 hidden rounded -inset-x-6 -inset-y-4 block"
                  ></span>
                  <span
                    >{{ projects.title }}
                    <span class="inline-block">
                      {{ projects.titlesub }}
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        class="inline-block h-4 w-4 shrink-0 transition-transform -translate-y-1 translate-x-1 -translate-y-1 translate-x-1 transition-none ml-1 translate-y-px"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M5.22 14.78a.75.75 0 001.06 0l7.22-7.22v5.69a.75.75 0 001.5 0v-7.5a.75.75 0 00-.75-.75h-7.5a.75.75 0 000 1.5h5.69l-7.22 7.22a.75.75 0 000 1.06z"
                          clip-rule="evenodd"
                        ></path>
                      </svg>
                    </span>
                  </span>
                </a>
              </h3>
              <p class="mt-2 text-sm leading-normal">
                <ol style="list-style: disc;margin-left: 20px;">
                  <li v-for="dets in projects.details" :key="dets">{{ dets }}</li>
                </ol>
              </p>
              <ul class="flex flex-wrap related" aria-label="Related links">
                <li class="mr-4" v-for="types in projects.type" :key="types">
                  <span
                    class="relative inline-flex items-center text-sm font-medium text-slate-300"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 20 20"
                      fill="currentColor"
                      class="mr-1 h-3 w-3"
                      aria-hidden="true"
                    >
                      <path
                        fill-rule="evenodd"
                        d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                        clip-rule="evenodd"
                      ></path>
                    </svg>
                    <span>{{ types }}</span>
                  </span>
                </li>
              </ul>
              <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                <li
                  class="mr-1.5 mt-2"
                  v-for="techno in projects.tech"
                  :key="techno"
                >
                  <div
                    class="flex items-center rounded-full bg-teal-400 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                  >
                    {{ techno }}
                  </div>
                </li>
              </ul>
            </div>
            <img
              alt=""
              loading="lazy"
              width="200"
              height="48"
              decoding="async"
              data-nimg="1"
              class="rounded border-2 transition border-slate-200 order-1 col-span-2 translate-y-1"
              style="color: transparent; z-index: 9"
              :src="projects.thumb"
            />
          </div>
        </li>
      </ul>
      <ViewFullbtn title="Project Archive" link="/archives" />
    </div>
  </section>

  <section id="otherprojects">
    <div class="scroll-section mb-36 scroll-mt-24">
      <ul>
        <li class="mb-12" v-for="projects in otherproj.slice(0, 3)" :key="projects.title">
          <div
            class="proj-sec group relative grid grid-cols-8 gap-4 pb-1 transition-all gap-4 opacity-100 opacity-50"
          >
            <div
              class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none -inset-x-6 block bg-slate-800 drop-shadow-lg"
            ></div>
            <div class="z-10 order-2 col-span-6" style="grid-column: span 12/span 12;">
              <p class="text-sm leading-normal" style="margin: 0;">
                {{ projects.year }}
              </p>
              <h3>
                <a
                  class="inline-flex items-baseline font-medium leading-tight text-slate-200 text-base"
                >
                  <span
                    class="absolute -inset-x-4 -inset-y-2.5 hidden rounded -inset-x-6 -inset-y-4 block"
                  ></span>
                  <span
                    >{{ projects.title }}
                    <span class="inline-block">
                      {{ projects.titlesub }}
                    </span>
                  </span>
                </a>
              </h3>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import { defineComponent, ref } from "vue";
import { proj, otherproj } from "../utils/projects";
import ViewFullbtn from "../components/ViewFull.vue";

export default defineComponent({
  name: "ProjectsSection",

  components: { ViewFullbtn },

  setup() {
    return {
      proj,
      otherproj
    };
  },
});
</script>

<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";

img,
video {
  max-width: 100%;
  height: auto;
}
</style>
