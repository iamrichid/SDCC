<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import { MapPinIcon,PhoneIcon} from '@heroicons/vue/24/solid'
import TopBar from './components/TopBar.vue'
import MainNav from './components/MainNav.vue'
</script>

<template>
  <header>
 <TopBar />
 <MainNav />

  </header>

  <RouterView />

</template>

