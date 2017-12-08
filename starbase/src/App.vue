<template>
  <div id="app">
    <h3>{{ title }}</h3>
    <!-- <button class="btn btn-danger" v-on:click="fetchData">Fetch Data</button> -->
    <character v-bind:id="14" />
  </div>
</template>

<script>
import character from './components/character.vue'

export default {
  name: 'app',
  data() {
      return {
        title: "Genertate Your Team"
      }
  },
  components :{
     character
  }
}
</script>
