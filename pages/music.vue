<template>
  <div class="grid h-screen lg:place-items-center grid-cols-1">
    <!-- <h1 class="text-5xl text-center font-bold">{{ page.header }}</h1> -->

    <img v-if="page.mainImage" :src="page.mainImage" alt="a">
      <SanityContent
        class="max-w-2xl space-y-2 text-sm text-left"
        :blocks="page.richText"
       
      />
      
   
  </div>
</template>

<script>

import { groq } from "@nuxtjs/sanity";

const query = groq`*[_type=="music"][0]{
  "mainImage": mainImage.asset->url,
  richText
}`;

export default {

  data() {
    return {
    };
  },
  async asyncData({ $sanity  }) {
    const page =await $sanity.fetch(query)
    return {page}
  
   
  } 
};
</script>

<style>
</style>