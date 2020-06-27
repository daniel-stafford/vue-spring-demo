<template>
  <div id="app">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
    }
  },
  mounted() {
    fetch('http://localhost:8085/').then(response =>
      response.text().then(data => (this.title = data)),
    )
  },
}
</script>

<style>
#app {
  display: flex;
  justify-content: center;
}
</style>
