<template>
  <div v-editable="blok" class="pb-8 mb-6 font-bold text-center">
    <h2 class="text-6xl font-normal leading-normal mt-0 mb-2 text-blueGray-800">
      {{ blok.headline }}
    </h2>
    <p class="text-xl font-semibold leading-relaxed mt-6 mb-4 text-blueGray-800">
      {{ blok.paragraph }}
    </p>
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
