<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add'"
      :color="showAddTask ? 'red' : 'green'"
    ></Button>
    <!-- <Button text="Update Task" color="blue"></Button>
    <Button text="Delete Task" color="red"></Button> -->
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  components: { Button },
  name: "Header",
  props: { title: String, showAddTask: Boolean },
  emits: ["toggle-add-task"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>