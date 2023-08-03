<template>
  <div class="children">
    <div>Total Course Number</div>
    <div>{{ count }}</div>
    <div>Course Name:</div>
    <div>{{ courses.name }}</div>
    <div>Credit:</div>
    <div>{{ courses.credit }}</div>
    <div>Course ID:</div>
    <div>{{ courses.id }}</div>
    <div>Total Hours:</div>
    <div>{{ courses.hours }}</div>
    <div>Course Description:</div>
    <div>{{ courses.description }}</div>
    <div>Instructor:</div>
    <div>{{ courses.teacher }}</div>
    <div>Course Availability:</div>
    <div>{{ courses.full }}</div>
    <!-- <button @click="outerAdd">Add</button> -->
    <button @click="innerAdd">Add</button>
    <button @click="innerRemove">Remove</button>
  </div>
</template>

<script>
export default {
  name: "CourseItem",
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
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "5",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
        {
          name: "Web Design Specialist",
          credit: "20",
          id: "6",
          hours: "60",
          description: "This is a intensive web design course",
          teacher: "Peter",
          full: "false",
        },
      ],
    };
  },
  methods: {
    innerAdd() {
      this.count++;
    },
    innerRemove() {
      this.count--;
    },
    // outerAdd() {
    //   this.$emit("count-to-parent");
    // },
  },
};
</script>

<style lang="scss">
.children {
  width: 200px;
  height: 300px;
  border: 1px solid black;
  word-wrap: break-word;
}
</style>
