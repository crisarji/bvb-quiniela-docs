<template>
  <div v-editable="blok" class="prose my-4 mx-auto p-2">
    <div>
      <h1>{{ blok.name }}</h1>
      <rich-text-renderer :document="blok.intro" />
      <img class="w-64 h-128 float-none" :src="blok.image1.filename" alt="" />
      <rich-text-renderer :document="blok.body" />
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
  }
};
</script>
