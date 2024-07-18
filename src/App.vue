<script setup>
import { ref } from 'vue';
import MainCard from "./components/MainCard.vue";
import ProjectsCard from "./components/ProjectsCard.vue";
import ResumeCard from "./components/ResumeCard.vue";

const projectsRef = ref(null);
const resumeRef = ref(null);

const scrollToSection = (section) => {
  if (section === "projects" && projectsRef.value) {
    projectsRef.value.scrollIntoView({ behavior: "smooth" });
  } else if (section === "resume" && resumeRef.value) {
    resumeRef.value.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<template>
  <div class="main-container">
    <MainCard @scroll-to-section="scrollToSection" />
    <div ref="projectsRef">
      <ProjectsCard />
    </div>
    <div ref="resumeRef">
      <ResumeCard />
    </div>
  </div>
  <!--
  <MainCard />
  <ProjectsCard />
  <ResumeCard />
  -->
</template>

<style>
</style>
