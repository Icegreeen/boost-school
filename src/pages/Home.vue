<script setup>
import courses from "../courses";
import CourseSummary from "../components/CourseSummary.vue";
</script>

<template>
  <div class="Home page">
    <header>
      <Navbar />
    </header>
    <CourseSummary
      v-for="course in courses"
      :key="course.id"
      :course="course"
    />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";

export default {
  components: {
    Navbar,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "montserrat", sans-serif;
}

header {
  width: 100vw;
  background-color: #222;
  padding: 15px;
}
</style>
