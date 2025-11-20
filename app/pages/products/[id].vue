<template>
  <div class="product-details">
    <v-card v-if="data">
      <img
        :src="data.thumbnail"
        alt="img"
        height="200"
        class="w-100"
        style="object-fit: contain"
      />
      <v-card-title>{{ data.title }}</v-card-title>
      <v-card-text>Price: ${{ data.description }}</v-card-text>
    </v-card>
  </div>
</template>

<script setup>
const { data, error } = useFetch(
  `https://dummyjson.com/products/${useRoute().params.id}`
);

if (error.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}
</script>
