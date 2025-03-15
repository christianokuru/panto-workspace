<script setup>
definePageMeta({
  loading: true
})

await new Promise(resolve => setTimeout(resolve, 2000))
</script>

<template>
  <div>
    
    <h1 class="text-center text-3xl mt-10">About Page</h1>
  </div>
</template>
