<template>

  <!-- <h1>Ich bin eine Todo Liste</h1> -->

  <TodoInput
  @addTodo="writeTodo($event)"
  myplaceholder="Bitte Todo eingeben ..."
  > </TodoInput>


  <div class="todoliste">

    <p v-if="countTodos == 0">Die Liste ist noch leer! 😢 </p>

    <p v-else> 🤹 Du hast heute noch {{countTodos}} Aufgaben zu erledigen</p>

    <li
    @click="deleteTodo(index)"
    v-for="item, index in todos"
    :id="index"
    class="todo">

    {{ item }}

  </li>

</div>

</template>

<script>
import TodoInput from '@/components/TodoInput.vue'

export default {
  name: 'TodoList',
  components: {
    TodoInput
  },
  data() {
    return {
      todos: ["Einkaufen", "Vue", "Feierabend"],
    }
  },
  methods: {
    writeTodo(todo){

      // write todo to array
      this.todos.push(todo);

      // console.log(this.todos);

    },

    deleteTodo(index){

      this.todos.splice(index, 1);

      // console.log("Lösche Todo: " + index);

    },

  },
  computed: {

    countTodos(){

      return this.todos.length;

    }

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1{
  color: red;
}

.todoliste{

  text-align: left;

}

.todo{
  cursor: pointer;
}

</style>
