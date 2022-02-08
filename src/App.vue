<template>
  <input type="text" ref="name">
  <button @click="handleClick">click me</button>
</template>

<script>
export default {
  name: 'App',
  methods: {
    handleClick() {
      alert(this.$refs.name.value)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
