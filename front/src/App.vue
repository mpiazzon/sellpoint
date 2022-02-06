<template>
  <v-layout>
    <v-app-bar density="compact" absolute>
      <v-app-bar-title>Vuetify</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn text><router-link to="/">venta</router-link></v-btn>
      <router-link to="/about">productos</router-link>

      <v-btn class="mr-4 ml-5" color="primary" plain>
        <v-icon left icon="mdi-handshake-outline"></v-icon>

        <span>salir</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-layout>
</template>
