<template>
  <v-app>
    <v-app-bar app>
      <ul class="d-flex" style="gap: 20px">
        <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
        |
        <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
        |
        <NuxtLink :to="{ name: 'profile' }">Profile</NuxtLink>
        |
        <NuxtLink :to="{ name: 'products' }">Products</NuxtLink>
      </ul>
    </v-app-bar>

    <v-main>
      <div class="about-layout">
        <slot />
      </div>
    </v-main>

    <v-footer app>
      <ul class="d-flex" style="gap: 20px">
        <NuxtLink :to="{ name: 'index' }">Home</NuxtLink>
        <NuxtLink :to="{ name: 'about' }">About</NuxtLink>
        <NuxtLink :to="{ name: 'profile' }">Profile</NuxtLink>
        <NuxtLink :to="{ name: 'products' }">Products</NuxtLink>
      </ul>
    </v-footer>
  </v-app>
</template>
