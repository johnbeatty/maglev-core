<template>
  <icon :name="iconName" />
</template>

<script>
export default {
  name: 'PageIcon',
  props: {
    page: { type: Object, required: true },
    size: { type: String, default: '1.25rem' },
  },
  computed: {
    iconName() {
      return this.isIndexPage ? 'home-4-line' : 'ri-file-line'
    },
    isIndexPage() {
      return this.services.page.isIndex(this.page)
    },
  },
}
</script>
