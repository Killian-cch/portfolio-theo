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
  </div>
  <div class="table-contents">
    <div class="title">
      <img alt="" class="bullet-point" src="@/assets/images/two_stars.svg"/>
      <div>Sommaire</div>
    </div>
    <ul>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Branding & Infographie</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Packaging & patron</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>UI & UX Design</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Créations Digitales</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Création Plastique</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Photographie</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
      <li>
        <a href="#">
          <div class="big-wrap">
            <div class="wrap">
              <img alt="" class="hover-star" src="@/assets/images/star_hover.svg"/>
              <span>Autres, experimentations...</span>
            </div>
            <img alt="" class="arrow-tr" src="@/assets/images/arrow_tr.svg"/>
          </div>
        </a>
      </li>
    </ul>
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
        max-width: 700px
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
      padding: 0 4rem
      display: flex
      flex-flow: row nowrap
      align-items: center
      column-gap: 1rem
      margin-bottom: 3rem
      
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
        transition: all 0.3s ease
        a
          display: block
          font-family: Stylish Delight
          margin: 0 6rem
          padding: 2rem 0
          text-decoration: none
          color: white
          font-size: 2.25rem
          border-top: solid 1px #313131
          .big-wrap
            display: flex
            flex-flow: row nowrap
            justify-content: space-between
            align-items: center
            padding: 0 4rem
            .wrap
              display: flex
              flex-flow: row nowrap
              justify-content: space-between
              align-items: center
              column-gap: 2rem

              .hover-star
                width: 60px
                opacity: 0
            .arrow-tr
              transition: all 0.3s ease
              width: 33px
        &:hover
          background-color: white
          a
            border-top: solid 1px rgba(0, 0, 0, 0)
            *
              color: #1D1D1D
            .big-wrap
              .wrap
                .hover-star
                  opacity: 1
              .arrow-tr
                filter: invert(100%)
                width: 44px
      
        &:last-child
          a
            border-bottom: solid 1px #313131
          &:hover
            a
              border-bottom: solid 1px rgba(0, 0, 0, 0)


         
            

</style>