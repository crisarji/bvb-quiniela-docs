<template>
  <div v-editable="blok" class="pb-8 mb-6 text-left">
    <h1 class="text-2xl font-normal leading-normal mt-0 mb-2 text-blueGray-800">
      {{ blok.headline }}
    </h1>
    <rich-text-renderer :document="blok.paragraph" />
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
