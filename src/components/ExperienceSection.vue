<template>
  <section id="experience">
    <div class="scroll-section mb-36 scroll-mt-24">
      <ol>
        <li class="mb-12" v-for="experience in expe" :key="experience.year">
          <div
            class="group relative grid pb-1 transition-all grid-cols-8 gap-4"
          >
            <div
              class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition -inset-x-6 block drop-shadow-lg bg-slate-800"
            ></div>
            <header
              class="z-10 mb-2 mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500 col-span-2"
              aria-label="2018 to Present"
            >
              {{ experience.year }}
            </header>
            <div class="z-10 col-span-6">
              <h3 class="font-medium leading-snug text-slate-200 m-0">
                <div class="ln-0">
                  <a
                    class="inline-flex items-baseline font-medium leading-tight text-slate-200 text-base"
                    :href="experience.url"
                    target="_blank"
                    rel="noreferrer"
                    aria-label="Lead Engineer at Upstatement"
                  >
                    <span
                      class="absolute -inset-x-4 -inset-y-2.5 hidden rounded -inset-x-6 block"
                    ></span>
                    <span
                      >{{ experience.position }} ·
                      <span class="inline-block">
                        {{ experience.company }}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 20 20"
                          fill="currentColor"
                          class="thesvg inline-block h-4 w-4 shrink-0 transition-transform"
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
                </div>
                <div>
                  <div class="text-slate-500" aria-hidden="true">
                    {{ experience.posdetails }}
                  </div>
                </div>
                <!-- <div>
                  <div class="text-slate-500" aria-hidden="true">Engineer</div>
                </div> -->
              </h3>
              <p class="mt-2 text-sm leading-normal">
                {{ experience.details }}
              </p>
              <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                <li
                  class="mr-1.5 mt-2"
                  v-for="techno in experience.tech"
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
          </div>
        </li>
      </ol>
      <ViewFullbtn title="Resume" link="/resume" targets="_blank" />
    </div>
  </section>
</template>
<script>
import { defineComponent } from "vue";
import { expe } from "../utils/experience";
import ViewFullbtn from "../components/ViewFull.vue";

export default defineComponent({
  name: "ExperienceSection",

  components: { ViewFullbtn },

  setup() {
    return {
      expe,
    };
  },
});
</script>
<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>
