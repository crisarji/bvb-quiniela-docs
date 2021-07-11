<template>
  <nuxt-link
    :to="articleLink"
    class="article-teaser block py-4 px-6 border rounded border-gray-500"
  >
    <div class="m-3">
      <h2 class="text-lg font-bold">
        {{ articleContent.name }}
        <span
          class="text-sm text-teal-800 font-mono bg-teal-100 inline rounded-full px-2 align-top float-right animate-pulse"
          >ReadMore</span
        >
      </h2>
      <rich-text-renderer :document="articleContent.intro" />
    </div>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    articleContent: {
      type: Object,
      required: true
    },
    articleLink: {
      type: String,
      required: true
    }
  }
};
</script>

<style>
/* .article-teaser:hover {
  box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.75);
} */
</style>
