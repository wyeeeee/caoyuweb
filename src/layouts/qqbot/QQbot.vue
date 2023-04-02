<template>
    <v-app id="inspire">
        <v-navigation-drawer v-model="drawer" color="white" floating>
          <DrwaerBar></DrwaerBar>
        </v-navigation-drawer>
    
        <v-app-bar color="white" >
          <v-app-bar-nav-icon color="black" @click="drawer = !drawer"></v-app-bar-nav-icon>
          <v-responsive
          class="ml-6 d-none d-sm-flex"
          max-width="150">
          <v-toolbar-title class="" >赛博曹宇QQBot</v-toolbar-title>
          </v-responsive>
          <v-responsive
          class="ml-6"
          max-width="344">
        <v-text-field clearable
        density="compact"
         class="pt-3 mx-auto" 
         label="搜索"
          variant="outlined"
         append-inner-icon="mdi-magnify" @click:append-inner="onClick"></v-text-field>
        </v-responsive>
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
