<template>
  <nav>
    <div class="grid pl-4 lg:pl-6 h-58 py-14 nav">
      <NuxtLink class="font-bold mb-6" to="/"> Tomás Epifani </NuxtLink>
      <div class="grid space-y-2">
        <NuxtLink to="/lives"> Lives </NuxtLink>
        <NuxtLink to="/news"> News </NuxtLink>
        <NuxtLink to="/music"> Music </NuxtLink>
      </div>
    </div>
  </nav>
</template>

<script>
</script>

<style scoped>
.nav a {
  
  text-decoration: none !important;
   background: linear-gradient(currentColor 0 0) 0 100% / var(--d, 0) 1px
    no-repeat;
  transition: 0.5s;
}
.nav .grid a{
  width: 40px;
}
a.nuxt-link-exact-active {
  color: #6d6d6d;
}

.basic-1 {
  background: linear-gradient(currentColor 0 0) 0 100% / var(--d, 0) 3px
    no-repeat;
  transition: 0.5s;
}
.nav a:hover {
  --d: 100%;
}


</style>