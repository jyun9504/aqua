<template>
  <div class="home">
    <Header />
    Home
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/layouts/Header.vue'

export default {
  name: 'Home',
  components: {
    Header,
  }
}
</script>
