<template>
  <nuxt-content :document="doc" />
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const doc = await $content(params.slug || 'forms').fetch()

    return { doc }
  },
}
</script>

<style lang="scss">
table {
  border-collapse: separate;
  border-spacing: 2em 0;
}
</style>
