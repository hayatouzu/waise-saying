<template>
  <section>
    <CAnime />
    <CGame />
    <CMovie />
    <CPerson />
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
