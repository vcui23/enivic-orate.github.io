<template>
  <div id="index-page">
    <div class="main-container toflex">
      <div class="left-sect">
        <div>
          <FixHeader />
          <NavBar />
        </div>
        <div>
          <SocialIcons />
        </div>
      </div>

      <div class="right-sect">
        <AboutSection />
        <ExperienceSection />
        <ProjectsSection />
        <ShortDesc />
      </div>
    </div>
    <LandingPage />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import LandingPage from "../components/LandingPage.vue";
import AboutSection from "../components/AboutSection.vue";
import ProjectsSection from "../components/ProjectsSection.vue";

import FixHeader from "../components/FixHeader.vue";
import ExperienceSection from "../components/ExperienceSection.vue";
import ShortDesc from "../components/ShortDescSection.vue";
import SocialIcons from "../components/SocialIcons.vue";
import NavBar from "../shared/NavBar.vue";

import { scrollToTop } from "../utils/helpers";

export default defineComponent({
  name: "IndexPage",

  components: {
    // LandingPage,
    AboutSection,
    ProjectsSection,

    FixHeader,
    ExperienceSection,
    ShortDesc,
    SocialIcons,
    NavBar,
  },

  mounted() {
    scrollToTop();
  },

  methods: {
    scrollBack() {
      // smooth scroll
      window.scrollTo({
        top: 0,
        behavior: "smooth",
        block: "start",
        inline: "start",
      });
    },
  },
});
</script>

<style lang="scss" scoped>
.after-landing {
  width: 100%;
  max-width: 1024px;
  margin: 0 auto;
}

.scroll-back-btn {
  position: fixed;
  visibility: hidden;
  bottom: 20px;
  z-index: 99;
  right: 17%;
}

@media only screen and (max-width: 575px) {
  .scroll-back-btn {
    right: 10%;
  }
}
</style>
