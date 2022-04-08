<template>
  <form @submit.prevent="addItemAndClear(todo)">
    <input v-model="todo" type="text" /><button>Add</button>
  </form>
</template>

<script lang="ts">
import { ref, defineComponent } from "vue";
import { useTodoListStore } from "../store/useTodoListStore";
export default defineComponent({
  setup() {
    const todo = ref("");
    const store = useTodoListStore();

    function addItemAndClear(item: string) {
      if (item.length === 0) {
        return;
      }
      store.addTodo(item);
      todo.value = "";
    }

    return { todo, addItemAndClear };
  },
});
</script>

<style lang="scss" scoped></style>
