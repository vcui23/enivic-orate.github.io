<template>
  <div id="about-me" class="about-section">
    <div class="q-mt-md">
      <AvatarDisplay />
      <br /><br />
      <div class="content-div">
        <div class="about-header text-h4 text-weight-bold">Ernivic Orate</div>
        <div class="changing-text">
          call me <span style="color: rgb(94 234 212/1)">Hi, I am Vic</span>
        </div>
        <span class="opac-7">
          I am frontend developer doing all things creative to make beautiful
          application and make the web a more unique and awesome place.
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";
//   import { getImgUrl, randomNumber } from "../utils/helpers";
import { animateFunc } from "../utils/helpers";
import AvatarDisplay from "./AvatarDisplay.vue";

export default defineComponent({
  name: "FixHeader",

  components: { AvatarDisplay },

  setup() {
    return {
      // years: ref(new Date().getFullYear() - 2018),
      // pics: ref(["dp_primary.jpg", "dp_secondary.jpg"]),
    };
  },

  // methods: {
  //   isHandset() {
  //     return screen.width <= 575 ? true : false;
  //   },

  //   getImgUrl,
  //   randomNumber,
  // },
  mounted() {
    this.animateFunc();
  },

  methods: {
    isHandset() {
      return screen.width <= 575 ? true : false;
    },

    animateFunc,
  },
});
</script>

<style lang="scss" scoped>
.about-header {
  font-size: 3rem;
  line-height: 1;
  letter-spacing: -1px;
  color: #ffffffd6;
}
#about-me {
  font-size: 16px;
}
.about-section {
  margin-bottom: 64px;
}
.section {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.image-div {
  width: 40%;
  max-width: 40%;
  align-content: center;
  text-align: center;
  flex-grow: 1;
}
.content-div {
  width: 60%;
  max-width: 60%;
  margin-right: 24px;
  align-content: center;
  flex-grow: 1;
  line-height: 30px;
}
.href-link {
  text-decoration: none;
}
.href-link:hover {
  text-decoration: underline;
}
.sub-label {
  padding-right: 6px;
  color: #6c757d;
  font-weight: bold;
}

@media only screen and (max-width: 575px) {
  #about-me {
    font-size: 14px;
  }
  .about-section {
    margin-top: 24px;
    margin-bottom: 32px;
  }
  .section {
    flex-direction: column;
    text-align: center;
    padding: 16px;
  }
  .image-div {
    width: 100%;
    max-width: 100%;
  }
  .content-div {
    width: 100%;
    max-width: 100%;
    text-align: left;
  }
  .about-header {
    margin-top: 24px;
  }
}
</style>
