<template>
  <div class="bg-black h-screen px-6 py-12">
    <h2
      class="text-white font-exo text-5xl opacity-0"
      ref="title"
      style="transform: translateY(30px)"
    >
      MY WORK
    </h2>
    <div class="flex space-x-4">
      <div
        ref="projects"
        v-for="project in projects"
        class="w-full opacity-0"
        style="transform: translateX(30px)"
      >
        
          <a :href= "project.link"> 
          <img
            :src="project.image.url"
            alt="GitHub"
            style="height: 70vh"
            class="object-cover"
          />
          <p class="text-white font-space-mono text-sm">{{ project.title }}</p>
          </a>
        
      </div>
    </div>
  </div>
</template>
<script>
import gsap from "gsap";
import github3Img from "~/assets/github3.gif";
import AeImg from "~/assets/Ae.gif";
import AiImg from "~/assets/Ai.gif";
import youtubeImg from "~/assets/youtube.gif";
import PsImg from "~/assets/Ps.gif";
import codepjImg from "~/assets/codepj.gif";
import resugifImg from "~/assets/resugif.gif";
export default {
  data() {
    return {
      projects: [
        {
          image: {
            url: github3Img,
          },
          title: "GITHUB",
          link: "https://github.com/DanieljM95"
        },
        {
          image: {
            url: AeImg,
          },
          title: "AFTER EFFECTS",
          link: "/afterfx"
        },
        {
          image: {
            url: AiImg,
          },
          title: "ADOBE ILLUSTRATOR",
          link: "https://github.com/DanieljM95"
        },
        {
          image: {
            url: youtubeImg,
          },
          title: "YOUTUBE",
          link: "https://github.com/DanieljM95"
        },
        {
          image: {
            url: PsImg,
          },
          title: "ADOBE PHOTOSHOP",
          link: "https://github.com/DanieljM95"
        },
        {
          image: {
            url: codepjImg,
          },
          title: "CODING PROJECTS",
          link: "https://github.com/DanieljM95"
        },
        {
          image: {
            url: resugifImg,
          },
          title: "RESUME",
          link: "https://github.com/DanieljM95"
        },
      ],
    };
  },
  mounted() {
    gsap.to(this.$refs.title, {
      opacity: 1,
      duration: 1.5,
      y: 0,
      ease: "expo",
    });

    gsap.to(this.$refs.projects, {
      opacity: 1,
      duration: 1.5,
      stagger: 0.1,
      x: 0,
      ease: "expo",
      delay: 0.3,
    });
  },
};
</script>