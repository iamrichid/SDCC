<script setup>
import { MapPinIcon, PhoneIcon } from '@heroicons/vue/24/solid'
</script>

<template>
<div class="hidden sm:inline">
  <div class="flex p-2 justify-between bg-amber-800 text-white text-sm">
    <!-- Left: Location & Phone -->
    <div class="flex items-center gap-4">
      <div class="flex items-center">
        <MapPinIcon class="w-4 h-4 mr-1" />
        <span class="hidden sm:inline">No. F155/6, Orphans’ Crescent, North Labone, Accra. (View map)</span>
        <span class="sm:hidden font-semibold">Location</span>
      </div>

      <div class="flex items-center gap-1">
        <PhoneIcon class="hidden sm:inline w-5 h-5" />
        <span class="hidden sm:inline">+233 (0) 302 786 754</span>
        <a
          href="tel:+233302786754"
          class="sm:hidden inline-flex items-center gap-2 bg-blue-500 text-white py-1 px-3 rounded hover:bg-blue-600"
        >
          <PhoneIcon class="w-5 h-5" /> Call Now
        </a>
      </div>
    </div>

    <!-- Right: Socials -->
    <div class="flex items-center space-x-3">
      <SocialIcon href="https://twitter.com" color="hover:text-blue-400" />
      <SocialIcon href="https://facebook.com" color="hover:text-blue-600" name="facebook" />
      <SocialIcon href="https://linkedin.com" color="hover:text-blue-500" name="linkedin" />
      <SocialIcon href="#" color="hover:text-orange-500" name="rss" />
    </div>
  </div>

</div>

</template>
