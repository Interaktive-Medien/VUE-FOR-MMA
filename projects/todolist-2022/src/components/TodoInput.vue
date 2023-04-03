<template>

  <!-- <h1>Ich bin der Todo Input</h1> -->

  <input
  :placeholder="myplaceholder"
  v-model="myinput"
  type="text">

  <!-- <p> {{myinput}} </p> -->

  <button
  @click="submit()">
  + Hinzufügen</button>

</template>

<script>
export default {
  name: 'TodoInput',
  emits: ['addTodo'],
  props: ['myplaceholder'],
  data() {
    return {
      myinput: "",
    }
  },
  methods: {
    submit(){

      // console.log("Der Input ist: " + this.myinput);

      this.$emit('addTodo', this.myinput);

    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1{
  color: red;
}

</style>
