<template>
  <div class="container flex items-center">
    <div class="w-1/2 text-center">
      <nuxt-link
        to="/category/anime"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full"
      >
        偉人 名言
      </nuxt-link>
      <p>ここは偉人の名言を書くところです。</p>
    </div>
    <div class="c-person__image w-1/2"></div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-person__image {
  height: 100vh;
  width: 50%;
  background-image: url('~assets/images/topImages/anime.jpg');
}
</style>
