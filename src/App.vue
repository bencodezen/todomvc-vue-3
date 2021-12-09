<script>
import AppFooter from './components/AppFooter.vue'
import TodoApp from './components/TodoApp.vue'

export default {
  name: 'App',

  // Define components that will be used in the template
  components: {
    AppFooter,
    TodoApp
  },

  // Set the page title when the app is loaded
  created() {
    window.document.title = 'TodoMVC (Vue 3) by @bencodezen'
  }
}
</script>

<template>
  <TodoApp />
  <AppFooter />
</template>

<style>
@import './styles/todomvc-base.css';
@import './styles/todomvc-index.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.btn {
  padding: 0 10px;
}
</style>
