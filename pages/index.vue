<template>
  <section class="container mx-auto">
    <CAnime />
    <CGame />
    <CPerson />
    <CMovie />
  </section>
</template>

<script>
import CAnime from '@/pages/-CAnime'
import CGame from '@/pages/-CGame'
import CMovie from '@/pages/-CMovie'
import CPerson from '@/pages/-CPerson'

export default {
  components: {
    CAnime,
    CGame,
    CPerson,
    CMovie,
  },
}
</script>
