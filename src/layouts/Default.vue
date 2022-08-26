<template>
  <main>
    <HeaderComponent />
    <section>
      <slot />
    </section>
  </main>
</template>

<script>
import HeaderComponent from '@/components/Header.vue'
export default {
  name: 'DefaultLayout',
  components: {
    HeaderComponent
  }
}
</script>

<style lang="sass">

</style>
