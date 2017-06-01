<template>
  <v-app>
    <Drawer/>
  </v-app>
</template>

<script>
  import Drawer from './Drawer.vue'
  export default {
    data () {
      return {
      }
    },
    components: {
      Drawer
    }
  }
</script>

<style lang="scss">
  @import '../node_modules/vuetify/dist/vuetify.min.css'
</style>
