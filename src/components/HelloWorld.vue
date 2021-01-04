<template>
  <div class="hello">
    <h1>Hello World</h1>
    <p>hello</p>
  </div>
</template>

<script>
export default {
  name: "jpt",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
