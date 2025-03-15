<script setup>
import HeroComponent from '@/components/custom/HeroComponent.vue'
definePageMeta({
  loading: true
})

await new Promise(resolve => setTimeout(resolve, 2000))
</script>

<template>
    <div class="">
        <hero-component  />
    </div>
</template>