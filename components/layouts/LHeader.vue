<template>
  <header class="text-center bg-blue-200 w-full container mx-auto">
    <div class="container py-4">
      <h1>名言ツイート</h1>
      <p v-if="isTop">
        このサイトはカテゴリーごとに名言をランダムで表示します！<br />気に入ったものがあれば是非ツイートしてください！
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
