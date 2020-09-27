<template>
  <div class="container flex items-center">
    <div class="w-1/2 text-center">
      <nuxt-link
        to="/category/person"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full"
      >
        偉人 名言
      </nuxt-link>
      <p class="mt-10">
        このカテゴリーでは偉人の名言をランダムで表示していきます！
      </p>
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
  background-image: url('~assets/images/topImages/person.jpeg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
