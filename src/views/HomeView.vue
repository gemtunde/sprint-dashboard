<template>
  <v-app id="inspire" :style="{background: $vuetify.theme.themes.dark.background}">
    <side-bar />
    <side-bar-right />
  </v-app>
</template>

<script>
import SideBar from '@/components/SideBar.vue'
import SideBarRight from '@/components/SideBarRight.vue'

  export default {
    name: 'HomePage',

    components: {
        SideBar,
        SideBarRight,
    },
  }
</script>