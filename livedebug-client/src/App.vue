<template>
  <div id="app">
    <navigation :counter="this.favorites.length"/>
    <router-view @myFavorite="myFavorite" :favorites="favorites"/>
  </div>
</template>

<script>
import '@/assets/style.css'
import navigation from '@/components/Navigation'

export default {
  data () {
    return {
      favorites: []
    }
  },

  components: {
    navigation
  },

  methods: {
    myFavorite (data) {
      this.favorites = this.favorites.concat(data)
    }
  }
}
</script>

<style>
</style>
