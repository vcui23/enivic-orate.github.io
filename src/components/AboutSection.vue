<template>
  <section id="about">
    <div class="scroll-section about-section mb-36 scroll-mt-24">
      <p>
        Motivated, innovative, and proficient front end web developer with
        {{ years }}
        years’ programming experience and desire to partner with a technology
        startup with opportunities for long-term growth. Knowledgeable
        programmer seeking opportunities in software development and creative
        solutions design.
      </p>
    </div>
  </section>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "AboutSection",

  setup() {
    return {
      years: ref(new Date().getFullYear() - 2017),
    };
  },
});
</script>
<style>
.about-section p {
  font-size: 16px;
  opacity: 0.7;
  line-height: 30px;
}
</style>
