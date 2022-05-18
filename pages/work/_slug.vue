<template>
  <div class="bg-black h-screen px-6 py-12">
    <h2
      class="text-white font-exo text-5xl"
      ref="title"
      style="transform: translateY(30px)"
    >
      HTML FOR THIS PROJECT
    </h2>
  </div>
</template>
<script>
import gsap from "gsap";

export default {
  async asyncData({ params }) {
    // make your async call here
    // const {data} = axios.get(`/api/work/${params.slug}`)

    // return template data here
    // return { data };
    return;
  },
  data() {
    return {};
  },
  mounted() {},
};
</script>
