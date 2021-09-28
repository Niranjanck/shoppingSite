<template>
  <v-app>
    <NavBar />
    <Nuxt />
    <shopFooter />
  </v-app>
</template>
<script>
import shopFooter from '@/components/shopFooter.vue'
import NavBar from '@/components/NavBar.vue'

export default {
  components: {
    shopFooter,
    NavBar,
  },
}
</script>
