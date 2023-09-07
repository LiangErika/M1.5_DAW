<template>
  <v-app>
    <default-bar />

    <default-view />
    <SideBar />
  </v-app>
</template>

<script setup>
  import DefaultBar from './AppBar.vue'
  import DefaultView from './View.vue'
  import SideBar from '@/components/SideBar.vue'
</script>
