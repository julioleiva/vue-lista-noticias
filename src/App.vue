<template>
  <div class="container" id="app">


    <SourceSelection v-on:sourceChanged="sourceChanged"></SourceSelection>
    <Newslist v-bind:source="source"></Newslist>

    <div class="footer">
      <p>&copy <a href="http://jleiva.es" target="_blank">jleiva.es</a> </p>
    </div>
  </div>
</template>

<script>
import Newslist from './components/Newslist'
import SourceSelection from './components/SourceSelection'

export default {
  name: 'app',
  components: {
    Newslist,
    SourceSelection
  },
  data () {
    return {
      source: ""
    }
  },
  methods: {
    sourceChanged: function (source) {
      this.source = source;
    }
  }
}
</script>

<style>
  #app {
    padding-top: 20px
  }
</style>
