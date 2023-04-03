<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <Hello msg="Welcome to Your Vue.js App"/> -->

    <TodoList> </TodoList>


</div>
</template>

<script>
// @ is an alias to /src
import Hello from '@/components/HelloWorld.vue'
import TodoList from '@/components/TodoList.vue'

export default {
  name: 'HomeView',
  components: {
    Hello,
    TodoList
  },


}
</script>

<style media="screen">
h1{
  color: blue;
}
</style>
