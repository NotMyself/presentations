<template>
  <div id="app">

    <header>
      <router-link to="/">🏠</router-link>
      <router-link to="/login">🔐</router-link>
      <a href="#" @click.prevent="logout">🚪</a>
    </header>

    <h1>Demo Auth Vue</h1>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',

  methods: {
    logout () {
      window.localStorage.clear()
      this.$router.push({ name: '/login' })
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

header {
  text-align: left;
  border-bottom: 2px dotted #2c3e50;
}

header a {
  font-size: 2em;
  margin-left: 20px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a, .green {
  color: #42b983;
}

</style>
