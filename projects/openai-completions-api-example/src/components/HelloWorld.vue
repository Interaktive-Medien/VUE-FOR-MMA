<template>
  <div class="hello">
    <h1> Hallo Welt</h1>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  mounted() {

    this.fetchAPI();

  },

  methods: {



    fetchAPI() {

      // https://platform.openai.com/docs/api-reference/introduction
      // [{"role": "system", "content": "You are Donald Trump. Write like Donald Trump."}, {"role": "user", "content": "Hello!"}]

      fetch('https://api.openai.com/v1/chat/completions', {
        body: JSON.stringify({
          model: 'gpt-3.5-turbo',
          messages: [{"role": "user", "content": "Hello!"}],
          temperature: 0.3,
          max_tokens: 3000,
        }),

        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          Authorization: 'Bearer ' + 'your api key'
        }
      })
        .then((response) => {
          // console.log(response); //If you want to check the full response

          response.json().then((json) => {

            console.log(json.choices[0].message.content);

          });

        })
        .catch((error) => {

          console.error(error);
          console.log('there was an error!!')

        });

    }

  }

}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
