<template>
  <div class="flex flex-col h-screen">
    <Header />
    <Nuxt class="flex-grow"/>
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>
