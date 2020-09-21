<template>
  <section class="container mx-auto px-5">
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
import CPerson from '@/pages/-Cperson'

export default {
  components: {
    CAnime,
    CGame,
    CPerson,
    CMovie,
  },
}
</script>
