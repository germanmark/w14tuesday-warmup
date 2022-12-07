<template>
  <div id="app">
    <ToastNotification/>
    <PostButton/>
    <DeleteButton/>
  </div>
</template>

<script>
import DeleteButton from './components/DeleteButton.vue'
import PostButton from './components/PostButton.vue'
import ToastNotification from './components/ToastNotification.vue'

export default {
  name: 'App',
  components: {
    ToastNotification,
    DeleteButton,
    PostButton
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
