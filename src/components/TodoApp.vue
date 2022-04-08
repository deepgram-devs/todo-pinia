<template>
  <todo-form />
  <todo-list />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TodoForm from "./TodoForm.vue";
import TodoList from "./TodoList.vue";
export default defineComponent({
  components: { TodoForm, TodoList },
  setup() {
    return {};
  },
});
</script>
