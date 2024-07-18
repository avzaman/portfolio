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
  <div>
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
body {
  margin: 0;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
