<script setup>
import NavbarComponent from '@/components/custom/NavbarComponent.vue'
import FooterComponent from '@/components/custom/FooterComponent.vue'

const { progress, isLoading, error, start, finish, clear } = useLoadingIndicator({
    throttle: 900,
    duration: 1000
})
</script>

<template>
    <NuxtLoadingIndicator color="orange" height=2 />
  <div class="">
    <navbar-component />
    <nuxt-page />
    <footer-component />
  </div>
</template>
