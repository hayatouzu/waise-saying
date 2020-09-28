<template>
  <div class="category">
    <div v-if="saying" class="container mx-auto text-center flex-col">
      <p class="mt-10">名言：{{ saying.text }}</p>
      <!-- <div v-if="!saying.image" class="h-20"></div> -->
      <img
        v-if="saying.image"
        class="w-auto h-64 mx-auto mt-12 object-cover"
        :src="saying.image"
      />
      <p class="mt-4">作品：{{ saying.name }}</p>
    </div>
    <div v-if="!saying" class="sayigLargeButtonn text-center">
      <p class="text-xl mb-6">↓名言を表示！</p>
      <a
        href="#"
        class="inline-block bg-blue-500 hover:bg-blue-700 text-3xl text-white font-bold py-16 px-24 rounded-full"
        @click.prevent="getSaying"
      >
        名言ボタン
      </a>
    </div>
    <div v-if="saying" class="absolute sayingButton mt-10">
      <a
        href="#"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full"
        @click.prevent="getSaying"
      >
        名言ボタン
      </a>
      <a
        v-if="saying"
        target="_blanck"
        :href="tweet"
        class="ml-10 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full"
      >
        ツイートする
      </a>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    // paramsでアニメ、映画、偉人ymlを分けてデータを取ってきている「.caegory」で取ってきている
    const saying = await $content('saying', params.category)
    const sayingData = await saying.fetch()
    return { sayingData: sayingData.sayings }
  },
  data() {
    return {
      saying: null,
    }
  },
  computed: {
    tweet() {
      return `https://twitter.com/intent/tweet?text=${this.saying.text}&url=`
    },
  },
  methods: {
    getSaying() {
      const random = Math.round(Math.random() * (this.sayingData.length - 1))
      this.saying = this.sayingData[random]
    },
  },
}
</script>

<style lang="scss" scoped>
.sayingButton {
  transform: translateX(-50%);
  left: 50%;
  top: 70%;
}
.category {
  height: 70vh;
}
.sayigLargeButtonn {
  position: absolute;
  top: 31%;
  left: 34%;
}
</style>
