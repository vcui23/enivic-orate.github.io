<template>
  <div>
    <iframe
      title="PDF"
      width="100%"
      height="1000px"
      src="/Ernivic-Orate.pdf"
    ></iframe>
  </div>
</template>

<script>
export default {
  name: "MyResume",
  data() {
    return {
      documentUrl: "/ErnivicOrateResume.pdf",
    };
  },
};
</script>
