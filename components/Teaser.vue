<template>
  <div v-editable="blok" class="pb-8 mb-6 text-center">
    <h2 class="text-6xl font-normal leading-normal mt-0 mb-2 text-blueGray-800">
      {{ blok.headline }}
    </h2>
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
