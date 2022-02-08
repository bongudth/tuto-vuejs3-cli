<template>
  <button @click="toggleModal">open modal</button>
  <div v-show="showModal">
    <Modal
      :title="title"
      :content="content"
      :theme="theme"
      @close="toggleModal"
    />
  </div>
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
