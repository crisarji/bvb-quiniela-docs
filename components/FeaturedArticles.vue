<template>
  <div v-editable="blok">
    <h2 class="pt-2 pl-6 text-lg text-blueGray-700 font-bold">
      {{ blok.title }}
    </h2>
    <div class="container mt-4 mx-auto">
      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4"
      >
        <div
          v-for="article in sortedArticles"
          :key="article._uid"
          class="card m-2 cursor-pointer rounded-lg hover:border-opacity-0 transform hover:-translate-y-1 transition-all duration-200"
        >
          <article-teaser
            v-if="article.content"
            :article-link="article.full_slug"
            :article-content="article.content"
          />
          <p v-else class="px-4 py-2 text-white bg-red-700 text-center rounded">
            This content loads on save.
            <strong>Save the entry & reload.</strong>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true
    }
  },
  computed: {
    sortedArticles() {
      // Load reference data/content from store
      const featuredArticles = this.$store.state.articles.articles.filter(
        article => {
          return this.blok.articles.includes(article.uuid);
        }
      );

      // Enable the ordering of the article previews
      featuredArticles.sort((a, b) => {
        return (
          this.blok.articles.indexOf(a.uuid) -
          this.blok.articles.indexOf(b.uuid)
        );
      });

      return featuredArticles;
    }
  }
};
</script>
