<script>
export default {
  props: {
    label: {
      type: String,
      required: true
    }
  },
  data: () => ({
    newTodo: ''
  }),
  computed: {
    finalNewTodo() {
      return this.newTodo.trim()
    }
  },
  emits: {
    'add-todo': todo => todo.length > 0
  },
  methods: {
    addTodo() {
      this.$emit('add-todo', this.finalNewTodo)
      this.newTodo = ''
    }
  }
}
</script>

<template>
  <label for="new-todo-input" class="sr-only">{{ label }}</label>
  <input
    v-bind="$attrs"
    v-model="newTodo"
    :placeholder="label"
    @keyup.enter="addTodo"
    id="new-todo-input"
    class="new-todo"
    autocomplete="off"
    autofocus
  />
</template>

<style></style>
