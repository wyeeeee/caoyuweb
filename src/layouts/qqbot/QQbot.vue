<template>
    <v-app id="inspire">
        <v-navigation-drawer v-model="drawer">
          <DrwaerBar></DrwaerBar>
        </v-navigation-drawer>
    
        <v-app-bar>
          <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
    
          <v-toolbar-title>赛博曹宇QQBot</v-toolbar-title>
        </v-app-bar>
    
        <v-main>
            <router-view />
        </v-main>
      </v-app>
</template>

<script setup>
    import { ref } from 'vue'
    import { useDisplay } from 'vuetify'
    import DrwaerBar from './Drwaer.vue'
    const drawer = ref(null);
    
</script>
