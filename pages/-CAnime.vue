<template>
  <div class="flex items-center">
    <div class="c-anime__image w-1/2"></div>
    <div class="w-1/2 text-center">
      <nuxt-link
        to="/category/anime"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full"
      >
        アニメ・漫画 名言
      </nuxt-link>
      <p class="mt-10">
        このカテゴリーではアニメ・漫画の名言をランダムで表示していきます！
      </p>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-anime__image {
  height: 100vh;
  width: 50%;
  background-image: url('~assets/images/topImages/anime.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
