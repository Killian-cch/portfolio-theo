<script setup>
  import Hero from '@/components/Hero.vue'
</script>

<template>
  <Hero />
  <div class="content">
    <div class="about">
      <div class="decor">
        <span></span>
        <div>À propos</div>
      </div>
      <p>Créatif et passionné par l’art, 21 ans, basé en France. Aime le dessin et les créations graphique qui en découle. Adore réaliser des interfaces graphique et s’adapter aux utilisateurs.</p>
    </div>

    <div class="table-contents">
      <div class="title">
        <img alt="" class="bullet-point" src="@/assets/images/two_stars.svg"/>
        <div>Sommaire</div>
      </div>
      <ul>
        <li><a href="#"><span>Branding & Infographie</span><span>test</span></a></li>
      </ul>
    </div>
  </div>
</template>

<style lang="sass" scoped>
  @import "@/assets/styles/breakpoints.sass"
  .content
    margin: 0 auto
    padding: 0 4rem

    .about
      display: flex
      flex-flow: row wrap
      align-items: center
      justify-content: left
      column-gap: 2rem

      p
        font-size: 1.25rem
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
        font-size: 2rem

        > span
          aspect-ratio: 1 / 1
          width: 4.5rem
          height: 4.5rem
          border-radius: 100%
          background-color: white
    
    .table-contents
      margin-top: 7rem
      .title
        display: flex
        flex-flow: row nowrap
        align-items: center
        column-gap: 1rem
        
        .bullet-point
          height: 4.5rem

        > div
          display: flex
          font-family: Stylish Delight
          white-space: nowrap
          font-size: 2rem
      
      ul
        list-style: none
        padding: 0
        margin: 0
        li
          position: relative
          transition: all 0.3s ease
          a
            margin: 0 1rem
            display: flex
            font-family: Stylish Delight
            padding: 2rem 3rem
            flex-flow: row nowrap
            justify-content: space-between
            align-items: center
            text-decoration: none
            color: white
            font-size: 2.25rem
          &::before
            z-index: 1
            content: ''
            position: absolute
            top: 0
            left: 50%
            transform: translateX(-50%)
            width: 100vw
            height: 100%
          &:hover
            a *
              color: #1D1D1D
              z-index: 2
            &::before
              z-index: 1
              content: ''
              position: absolute
              top: 0
              left: 50%
              transform: translateX(-50%)
              width: 100vw
              height: 100%
              background-color: white


         
            

</style>