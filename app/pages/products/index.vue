<template>
  <div class="products">
    <h1>products page</h1>
    <v-container v-if="data">
      <v-row>
        <v-col cols="4" v-for="item in data.products" :key="item.id">
          <v-card :to="{ name: 'products-id', params: { id: item.id } }">
            <img :src="item.thumbnail" alt="img" height="200" class="w-100" />
            <v-card-title>{{ item.title }}</v-card-title>
            <v-card-text>Price: ${{ item.description }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup>
const { data } = useFetch("https://dummyjson.com/products");
</script>
