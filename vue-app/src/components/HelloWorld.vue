<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
   
    <h3>Here's our component state: {{ variable }}</h3>
    <ul>
      <li v-for="item in array" :key="item">{{ item }}</li>
    </ul>

    <button @click="handleClick">CLick to show another message</button>
    <div v-if="showDiv">I was conditionally rendered!</div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => ({
    variable: "Woah...",
    array: [ 1, 2, 3, 4, 5 ],
    showDiv: false,
  }),
  methods: {
    handleClick() {
      this.showDiv = true;
    },
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
</style>
