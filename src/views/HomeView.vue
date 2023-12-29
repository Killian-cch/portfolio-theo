<script setup>
  import Hero from '@/components/Hero.vue'
</script>

<template>
  <Hero />
  <div class="content">
    <div class="about">
      <div class="decor">
        <span></span>
        <div><span>à</span> propos</div>
      </div>
      <p>Créatif et passionné par l’art, 21 ans, basé en France. Aime le dessin et les créations graphique qui en découle. Adore réaliser des interfaces graphique et s’adapter aux utilisateurs.</p>
    </div>
  </div>
</template>

<style lang="sass" scoped>
  @import "@/assets/styles/breakpoints.sass"
  .content
    margin: 0 2rem

  .about
    display: flex
    flex-flow: row wrap
    align-items: center
    justify-content: left
    column-gap: 2rem

    p
      font-weight: 200
      width: 50%
      text-transform: uppercase

    .decor
      display: flex
      flex-flow: row nowrap
      justify-content: center
      align-items: center
      column-gap: 1rem
      font-family: Stylish Delight
      white-space: nowrap
      font-size: 1.5rem

      > div span
        text-transform: uppercase
        font-size: 2rem

      > span
        aspect-ratio: 1 / 1
        width: 50px
        height: 50px
        border-radius: 50px
        background-color: white
</style>