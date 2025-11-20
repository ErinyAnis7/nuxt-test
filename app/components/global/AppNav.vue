<template>
  <div>
    <nav
      style="
        padding: 20px 10px;
        background-color: #d3d3d394;
        display: flex;
        gap: 10px;
      "
    >
      <NuxtLink :to="{ name: 'index' }">Home</NuxtLink> |
      <NuxtLink :to="{ name: 'about' }">About</NuxtLink> |
      <NuxtLink :to="{ name: 'profile' }">Profile</NuxtLink> |
      <NuxtLink :to="{ name: 'products' }">Products</NuxtLink>
    </nav>
  </div>
</template>

<script>
export default {
  mounted() {
    // console.log(this.$router.options.routes);
  },
};
</script>

<style>
.router-link-active.router-link-exact-active {
  font-weight: bold;
  color: red;
}
</style>
