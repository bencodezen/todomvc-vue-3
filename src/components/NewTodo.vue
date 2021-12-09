<script>
import { computed, reactive } from 'vue'

export default {
  props: {
    label: {
      type: String,
      required: true
    }
  },
  emits: {
    'add-todo': todo => todo.length > 0
  },
  setup(props, { emit }) {
    const todoState = reactive({
      newTodo: '',
      finalNewTodo: computed(() => {
        return todoState.newTodo.trim()
      })
    })

    const addTodo = () => {
      emit('add-todo', todoState.finalNewTodo)
      todoState.newTodo = ''
    }

    return {
      addTodo,
      todoState
    }
  }
}
</script>

<template>
  <label for="new-todo-input" class="sr-only">{{ label }}</label>
  <input
    v-bind="$attrs"
    v-model="todoState.newTodo"
    :placeholder="label"
    @keyup.enter="addTodo"
    id="new-todo-input"
    class="new-todo"
    autocomplete="off"
    autofocus
  />
</template>

<style></style>
