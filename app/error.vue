<template>
  <div
    class="error d-flex justify-center align-center"
    style="min-height: 90vh"
  >
    <v-card class="pa-5 mx-auto text-center">
      <v-card-title class="text-h5">Error {{ error.statusCode }}</v-card-title>
      <v-card-title class="text-h5">{{ error.statusMessage }}</v-card-title>
      <v-btn class="mt-4" @click="clearErr"> Back Home </v-btn>
    </v-card>
  </div>
</template>

<script setup>
defineProps(["error"]);

//methods
const clearErr = () => {
  clearError({
    redirect: "/",
  });
};
</script>
