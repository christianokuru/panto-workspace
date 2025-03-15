<script setup>
import { useRoute } from 'vue-router'
import LogoComponent from '@/components/custom/LogoComponent.vue'

const route = useRoute()

const navLinks = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Services', path: '/services' },
  { name: 'Contact', path: '/contact' }
]
</script>

<template>
  <nav class="absolute mt-[40px] flex items-center justify-between px-[40px] z-10 w-full text-white">
    <div>
        <logo-component />
    </div>
    <div class="max-w-[478px] mx-auto flex justify-center space-x-[65px]">
      <nuxt-link
        v-for="link in navLinks" 
        :key="link.path" 
        :to="link.path"
        class="hover:text-[#E58411] transition text-[18px]"
        :class="{ 'text-[#E58411]': route.path === link.path }"
      >
        {{ link.name }}
      </nuxt-link>
    </div>
  </nav>
</template>
