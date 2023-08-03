<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <h1>Course List</h1>
  <h2>Total Course Number</h2>
  <p>{{ count }}</p>
  <div class="parent">
    <CourseItem
      v-for="course in courses"
      :course="course"
      :key="course.id"
      @count-to-parent="addOne"
      @count-from-parent="removeOne"
    />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import CourseItem from "./components/CourseItem.vue";

export default {
  name: "App",

  data() {
    return {
      count: 0,
      courses: [
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "0",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "1",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "2",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "3",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "4",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
      ],
    };
  },
  components: {
    // HelloWorld,
    CourseItem,
  },
  methods: {
    addOne() {
      this.count++;
    },
    removeOne() {
      this.count--;
    },
 
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
