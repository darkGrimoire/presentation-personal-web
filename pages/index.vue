<template>
  <div class="deck">
    <div class="reveal">
      <div class="slides">
        <section>Slide 1</section>
        <section>Slide 2</section>
      </div>
    </div>
  </div>
</template>

<script>
import Reveal from 'reveal.js'
import Markdown from 'reveal.js/plugin/markdown/markdown.esm.js'

export default {
  name: 'HomePage',
  mounted() {
    const deck = new Reveal(document.querySelector('.deck'), {
      plugins: [Markdown],
      embedded: true,
    })

    deck.initialize()
  },
}
</script>

<style scoped>
.deck {
  height: 100vh;
  width: 100vw;
}
</style>