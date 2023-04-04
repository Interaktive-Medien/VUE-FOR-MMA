<template>
    <div>
      
        <button @click="buttonClicked()"> {{title}} </button>

    </div>

</template>
  
<script>

  export default {
    name: 'MyButton',
    props: {
      title: String
    },
    data() {
      return {
        // Your data properties go here
      };
    },
    methods: {

        buttonClicked() {
            
            this.$emit('buttonClicked')

        }
      // Your methods go here
    },

  };

</script>

<style>
</style>