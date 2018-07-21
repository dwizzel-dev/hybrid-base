<template>
  <div class="home">
    <h1>{{ title }}</h1>
    <img class="img" src="static/home.jpg">
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      title: 'Walk With Me!',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  width: 100%;
}
.home .img{
  width:100%;
  height:auto;
}
h1, h2 {
  font-weight: bold;
  font-size:2.5em;
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
