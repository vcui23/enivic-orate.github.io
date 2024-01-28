<template><div></div></template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "SupportMe",
});
</script>

<style lang="scss" scoped>
#support-me {
  font-family: "Avenir";
  padding-bottom: 64px;
}
.support-me {
  width: 100%;
  max-width: 635px;
  margin: 0 auto;
}
.page-header {
  font-size: 3rem;
}

.content {
  border-radius: 12px;
  padding: 48px;
  background-color: rgba(244, 244, 246);
}
.content-header img {
  width: 35%;
  height: auto;
}
.pp-header img {
  width: 20%;
  height: auto;
}

.pp-btn {
  color: rgba(17, 47, 130);
  background-color: rgba(248, 211, 93);
}

@media only screen and (max-width: 575px) {
  #support-me {
    padding-bottom: 0;
  }
  .page-header,
  .page-info {
    padding-left: 16px;
    padding-right: 16px;
  }
  .page-header {
    font-size: 2rem;
  }
  .support-me {
    margin-bottom: 0;
    padding-bottom: 0;
  }

  .content {
    padding: 32px 16px;
    padding-bottom: 64px;
    border-radius: 0;
  }

  .content-header img {
    width: 50%;
    height: auto;
  }
  .pp-header img {
    width: 30%;
    height: auto;
  }
}
</style>
