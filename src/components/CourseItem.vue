<template>
  <div class="children">
    <div>Course Name:</div>
    <div>{{ course.name }}</div>
    <div>Credit:</div>
    <div>{{ course.credit }}</div>
    <div>Course ID:</div>
    <div>{{ course.id }}</div>
    <div>Total Hours:</div>
    <div>{{ course.hours }}</div>
    <div>Course Description:</div>
    <div>{{ course.description }}</div>
    <div>Instructor:</div>
    <div>{{ course.teacher }}</div>
    <div>Course Availability:</div>
    <div>{{ course.full }}</div>
    <button @click="outerAdd">Add</button>
    <button @click="outerRemove">Remove</button>
    <!-- <button @click="innerAdd">Add</button>
    <button @click="innerRemove">Remove</button> -->
  </div>
</template>

<script>
export default {
  name: "CourseItem",
  props: {
    course: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    // innerAdd() {
    //   this.count++;
    // },
    // innerRemove() {
    //   this.count--;
    // },
    outerAdd() {
      this.$emit("count-to-parent");
    },
    outerRemove() {
      this.$emit("count-from-parent");
    },
  },
};
</script>

<style lang="scss">
.children {
  width: 400px;
  height: 300px;
  border: 1px solid black;
  word-wrap: break-word;
}
</style>
