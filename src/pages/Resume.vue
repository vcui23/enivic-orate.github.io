<template>
  <div>
    <MyResume />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import MyResume from "../components/FileViewer.vue";
import { proj } from "../utils/projects";

export default defineComponent({
  name: "ResumePage",

  components: {
    MyResume,
  },
});
</script>
