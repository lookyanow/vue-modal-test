<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal">
    <Modal header="Sign up" :text="text" @close="toggleModal"/>
  </div>
  <div v-if="showModalTwo" @close="toggleModalTwo">
    <ModalTwo>
      <h1>ModalTwo</h1>
      <p>Some text from modaltwo</p>
    </ModalTwo>
  </div>
  <p>
    <button @click.alt="toggleModal">Open modal(alt)</button>
  </p>
  <p>
    <button @click="toggleModalTwo">Open Model 2</button>
  </p>
</template>

<!-- <script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script> -->

<script>

import Modal from './components/Modal.vue'
import ModalTwo from './components/ModalTwo.vue'

export default {
  name: 'App',
  components: { Modal },
  data(){
    return {
      title: 'Hello world from Vue',
      text: 'Test text string',
      showModal: false,
      showModalTwo: false,
    }
  },

  methods: {
    toggleModal(){
      this.showModal = !this.showModal
    },

    toggleModalTwo(){
      this.showModalTwo = !this.showModalTwo
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
