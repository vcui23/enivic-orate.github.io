<template>
  <nav style="display: block">
    <ul class="mt-16 w-max my-navi">
      <li class="active about">
        <a
          class="menu-item list group flex items-center py-3"
          @click="scrollTo('#about')"
        >
          <span
            class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
          ></span>
          <span
            class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200 opac-7"
            >ABOUT</span
          >
        </a>
      </li>
      <li class="experience">
        <a
          class="menu-item list group flex items-center py-3"
          @click="scrollTo('#experience')"
        >
          <span
            class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
          ></span>
          <span
            class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200 opac-7"
            >EXPERIENCE</span
          >
        </a>
      </li>
      <li class="projects">
        <a
          class="menu-item list group flex items-center py-3"
          @click="scrollTo('#projects')"
        >
          <span
            class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
          ></span>
          <span
            class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200 opac-7"
            >PROJECTS</span
          >
        </a>
      </li>
    </ul>
  </nav>
</template>
<script>
import { defineComponent, ref } from "vue";
import { useRoute, createRouter, createWebHistory } from "vue-router";

import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default defineComponent({
  name: "NavBar",
  // router,

  setup() {
    return {
      dropDownMenu: ref(false),
    };
  },

  computed: {
    currentRoute() {
      return useRoute().path;
    },
  },

  methods: {
    goHome() {
      this.$router.push("/").then(() => {
        this.$router.go();
      });
    },

    goTo(route) {
      this.$router.push(route);
      router.go(-100);
    },

    scrollTo(ref) {
      this.$router.push({ name: "home", hash: `${ref}` });
    },
  },

  mounted: function () {
    const sections = document.querySelectorAll("section");
    console.log("ayayayayaya", sections);

    const navLi = document.querySelectorAll(".my-navi li");

    console.log("ayayayayaya22", navLi);
    window.onscroll = () => {
      var current = "";

      sections.forEach((section) => {
        const sectionTop = section.offsetTop;
        if (scrollY >= sectionTop - 100) {
          current = section.getAttribute("id");
        }
      });

      navLi.forEach((li) => {
        // li.classList.add("active");
        li.classList.remove("active");
        if (li.classList.contains(current)) {
          li.classList.add("active");
        }
      });
    };
  },
});
</script>

<style lang="scss" scoped>
#navbar {
  font-family: "Avenir";
  background-color: rgba(255, 255, 255);
  backdrop-filter: blur(40px);
  border-bottom: 1.5px solid #f0effb;
}
.toolbar {
  width: 100%;
  max-width: 1024px;
  margin: 0 auto;
  padding-left: 16px;
  padding-right: 16px;
}
.logo-btn,
.nav-btn {
  font-size: 15px;
  cursor: pointer;
  font-weight: 500;
  color: #007bff;
  margin-right: 12px;
  text-decoration: none;
}
.nav-btn:hover,
.logo-btn:hover {
  color: #2356ad;
}
.logo-btn {
  font-weight: 700;
}
.active-link {
  color: #2356ad;
}

.menu-btn {
  // color: #534b84;
  color: #f9f9f9;
  background-color: #007bff;
  box-shadow: 10px 10px 20px rgba(0, 0, 0, 0.08);
  border-radius: 42.5px;
}

.dropdown-menu .q-item.q-router-link--active,
.dropdown-menu .q-item--active,
.dropdown-menu .active-q-item {
  color: #ffffff !important;
  background-color: #2356ad !important;
}

@media only screen and (max-width: 575px) {
  .logo-btn {
    font-size: 16px;
    font-weight: 600;
    margin-right: 0;
  }
  .toolbar {
    padding-left: 16px;
  }
}
</style>
