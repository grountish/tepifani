<template>
  <div class="grid place-items-start grid-cols-1 sm:pt-1 lg:pt-10 mb-10">
    <img :src="page.mainImage" class=" lg:w-10/12 self-end my-5" alt="a" />
    <SanityContent
      class="max-w-2xl space-y-2 text-sm lg:w-10/12 text-justify"
      :blocks="page.richText"
    />
  </div>
</template>

<script>
import { groq } from '@nuxtjs/sanity'

const query = groq`*[_type=="home"][0]{
  "mainImage": mainImage.asset->url,
  richText
}`

export default {
  data() {
    return {}
  },
  async asyncData({ $sanity }) {
    const page = await $sanity.fetch(query)
    return { page }
  },
}
</script>

<style>
</style>