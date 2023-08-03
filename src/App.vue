<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <h1>Course List</h1>
  <!-- <p>{{ count }}</p>-->
  <div class="parent">
    <CourseItem v-for="course of couses" :key="course.id" />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import CourseItem from "./components/CourseItem.vue";

export default {
  name: "App",
  data() {
    return {
      //  count: 0,
    };
  },
  components: {
    // HelloWorld,
    CourseItem,
  },
  methods: {
    // addOne() {
    //   this.count++;
    // },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.parent {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
</style>
