<template>
  <h1>{{title}}</h1>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Sign up for more datails</h1>
      <p>Exciting paths awaits you!</p>
    </Modal>
  </div>
  <p>Welcome...</p>
  <button @click.alt="toggleModal">open modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data () {
    return {
      title: 'My first vue App :)',
      header: 'Sign up for more datails',
      text: 'Exciting paths awaits you!',
      showModal: false
    }
  },
  methods: {
    toggleModal(){
      this.showModal = !this.showModal
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
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
