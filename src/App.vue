<template>
  <button @click="toggleModal">open modal</button>
  <teleport to=".modal" v-show="showModal">
    <Modal
      :theme="theme"
      @close="toggleModal"
    >
      <template v-slot:links>
        <a href="#">sign up</a>
        <a href="#">more info</a>
      </template>
      <h1>{{ title }}</h1>
      <p>{{ content }}</p>
    </Modal>
  </teleport>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      showModal: false,
      title: 'Ninja Pizza',
      content: 'We don\'t make pizza. We make ninjas.',
      theme: 'sale'
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  },
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
