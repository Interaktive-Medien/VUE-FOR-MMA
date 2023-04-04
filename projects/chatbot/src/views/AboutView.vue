<template>
  <h1> Todo List {{ count }}</h1>

  <form @submit.prevent="submit()">
    <input @input="hasError = false" v-model="userInput" type="text">
    <button> Submit </button>
  </form>

  <p v-if="hasError == true" class="errorMessage"> Bitte gib ein Todo ein. </p>

  <ul>
    <li @click="deleteTodo(index)" v-for="todo, index in todos"> {{ todo }} </li>
  </ul>

</template>

<script>
export default {
  name: 'AboutView',
  components: {

  },
  data() {
    return {

      userInput: '',
      todos: ["Vuejs Lernen", "Weinen", "Nach Hause Fahren"],
      hasError: false

    }
  },
  methods: {

    submit() {

      if (this.userInput !== '') {

        this.todos.push(this.userInput);

        localStorage.setItem('todos', JSON.stringify(this.todos));

        this.userInput = '';

      } else {
          
          this.hasError = true;

      }

    },

    deleteTodo(index){

      this.todos.splice(index, 1);
      localStorage.setItem('todos', JSON.stringify(this.todos));

    },

    getLocalStorage(){

      if (localStorage.getItem('todos')) {

        this.todos = JSON.parse(localStorage.getItem('todos'));

      } else {

        this.todos = [];
      }

    }

  },

  computed: {

    count(){

      return this.todos.length;

    }

  },

  mounted() {
    
    this.getLocalStorage();

  }


}

</script>

<style scoped>

.errorMessage {
  color: red;
}

</style>