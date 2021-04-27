<template>
  <nav>
     <div class="grid  pl-4 lg:pl-6 h-58 py-14 nav ">
    <NuxtLink class=" font-bold mb-6" to="/">
        Tomás Epifani
    </NuxtLink>
    <div class="grid space-y-2">
      <NuxtLink to="/lives">
        Lives
    </NuxtLink>
      <NuxtLink to="/news">
        News
    </NuxtLink>
      <NuxtLink to="/music">
        Music
    </NuxtLink>
    </div>
  </div>
  </nav>
 
</template>

<script>

</script>

<style scoped>
.nav a{
  text-decoration: none !important;
}
a.nuxt-link-exact-active {
  color: #6d6d6d;
}
</style>