<template>
  <header class="text-center bg-blue-200 w-full">
    <div class="container mx-auto py-4">
      <h1>名言ツイート</h1>
      <p v-if="isTop">
        ここにテキスト入れてください
      </p>
      <nuxt-link to="/">
        TOP
      </nuxt-link>
    </div>
  </header>
</template>

<script>
export default {
  computed: {
    isTop() {
      return this.$route.fullPath === '/'
    },
  },
  mounted() {
    console.log(this.$route)
  },
}
</script>

<style lang="scss" scoped></style>
