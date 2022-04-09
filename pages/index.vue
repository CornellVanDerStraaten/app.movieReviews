<template>
  <div class="bg-gray-200">
    {{ this.name }}
  </div>
</template>

<script>
export default {
  name: 'IndexPage',

  data() {
    return {
      name: 'Index Pagina'
    }
  },

  async fetch() {
    const response = await this.$axios.$get('/');
    this.name = response;
  }
}
</script>
