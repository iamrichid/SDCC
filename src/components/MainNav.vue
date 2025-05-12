<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'



const isOpen = ref(false)
</script>

<template>
  <nav class="bg-white shadow px-4 py-3">
    <div class="flex justify-between items-center">
      <!-- Logo -->
      <RouterLink to="/" class="flex items-center gap-2">
        <img src="@/assets/sdcclogo.png" alt="SDC Capital logo" class="hidden sm:inline h-10" />
        <span class="sm:hidden font-bold text-amber-800 text-2xl sm:text-5xl md:text-6xl">SDC CAPITAL</span>
      </RouterLink>

      <!-- Desktop nav -->
      <ul class="hidden sm:flex gap-7 items-center font-bold uppercase text-sm">
        <li><RouterLink to="/about">About us</RouterLink></li>
        <li><RouterLink to="/services">Services</RouterLink></li>
        <li><RouterLink to="/cm-fund">CM Fund</RouterLink></li>
        <li><RouterLink to="/contact">Contact</RouterLink></li>
        <li><RouterLink to="/forms">Forms</RouterLink></li>
        <li><RouterLink to="/support">Customer Service</RouterLink></li>
      </ul>

      <!-- Hamburger Icon -->
      <button @click="isOpen = !isOpen" class="sm:hidden text-amber-800 focus:outline-none">
        <component :is="isOpen ? XMarkIcon : Bars3Icon" class="w-8 h-8 stroke-3"  />
      </button>
    </div>

    <!-- Mobile menu -->
    <transition name="fade">
      <ul
        v-if="isOpen"
        class="flex flex-col gap-4 mt-4 font-bold uppercase text-sm sm:hidden text-amber-800"
      >
        <li><RouterLink to="/about" @click="isOpen = false">About us</RouterLink></li>
        <li><RouterLink to="/services" @click="isOpen = false">Services</RouterLink></li>
        <li><RouterLink to="/cm-fund" @click="isOpen = false">CM Fund</RouterLink></li>
        <li><RouterLink to="/contact" @click="isOpen = false">Contact</RouterLink></li>
        <li><RouterLink to="/forms" @click="isOpen = false">Forms</RouterLink></li>
        <li><RouterLink to="/support" @click="isOpen = false">Customer Service</RouterLink></li>
      </ul>
    </transition>
  </nav>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
