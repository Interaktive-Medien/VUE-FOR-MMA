<template>

  <h1> Score: {{ score }} </h1>

   <!-- 3) use the component -->
  <MyButton @buttonClicked="scoreIncrease()" title="Score Increase"> </MyButton>
  <MyButton @buttonClicked="scoreDecrease()" title="Score Decrease"> </MyButton>

</template>

<script>
// 1) import the component
import MyButton from '@/components/MyButton.vue'

export default {
  name: 'HomeView',
  components: {
    // 2) add it to the components object
    MyButton
  },
  data() {
    return {
     
      score: 0,

    }
  },
  methods: {

    scoreIncrease() {
      this.score++
    },
    scoreDecrease() {
      this.score--
    }

  }
}

</script>
