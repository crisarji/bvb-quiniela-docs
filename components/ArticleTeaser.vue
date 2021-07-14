<template>
  <nuxt-link
    :to="articleLink"
    class="article-teaser block py-4 px-6 border rounded border-gray-500"
  >
    <div class="m-3">
      <h2 class="text-lg font-bold">
        {{ articleContent.name }}
        <span
          class="text-sm text-black font-mono bg-yellow-500 inline rounded-full px-2 align-top float-right animate-pulse"
          >Read+</span
        >
      </h2>
      <p
        class="font-light font-mono text-sm text-gray-700 hover:text-gray-900 transition-all duration-200"
      >
        {{ articleContent.shortIntro }}
      </p>
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
