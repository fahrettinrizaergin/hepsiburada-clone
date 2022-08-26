<template>
  <DefaultLayout>
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </DefaultLayout>
</template>

<script>
// @ is an alias to /src
import DefaultLayout from '@/layouts/Default.vue'

export default {
  name: 'HomeView',
  components: {
    DefaultLayout
  }
}
</script>
