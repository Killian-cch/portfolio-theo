<script setup>
  import Hero from '@/components/Hero.vue'
  import BrandingInfographie from '@/components/BrandingInfographie.vue'

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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
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
      <div class="separator"></div>
    </ul>
  </div>

  <BrandingInfographie />
</template>

<style lang="sass" scoped>
  @import "@/assets/styles/breakpoints.sass"
  .content
    margin: 0 auto
    padding: 0 4rem
    @include breakpoint($s-screen)
      padding: 0 2rem

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
        @include breakpoint($s-screen)
          font-size: 0.875rem

      .decor
        display: flex
        flex-flow: row nowrap
        justify-content: center
        align-items: center
        column-gap: 1rem
        font-family: Stylish Delight
        white-space: nowrap
        font-size: 2rem
        @include breakpoint($s-screen)
          font-size: 1.25rem

        > span
          width: 50px
          height: 50px
          border-radius: 100%
          background-color: white
          @include breakpoint($s-screen)
            width: 30px
            height: 30px
    
  .table-contents
    margin-top: 7rem
    .title
      padding: 0 4rem
      display: flex
      flex-flow: row nowrap
      align-items: center
      column-gap: 1rem
      margin-bottom: 3rem
      @include breakpoint($s-screen)
        padding: 0 2rem
      
      .bullet-point
        height: 76px
        @include breakpoint($s-screen)
          height: 37px

      > div
        display: flex
        font-family: Stylish Delight
        white-space: nowrap
        font-size: 2rem
        @include breakpoint($s-screen)
          font-size: 1.25rem
    
    ul
      list-style: none
      padding: 0
      margin: 0
      li
        transition: all 0.3s ease
        display: flex
        flex-flow: row nowrap
        align-items: center
        justify-content: space-between
        min-height: 124px
        a
          display: block
          font-family: Stylish Delight
          margin: 0 6rem
          padding: 2rem 0
          text-decoration: none
          color: white
          font-size: 2.25rem
          width: 100%
          @include breakpoint($s-screen)
            margin: 0
            font-size: 1.5rem
          .big-wrap
            display: flex
            flex-flow: row nowrap
            justify-content: space-between
            align-items: center
            padding: 0 4rem
            width: 100%
            @include breakpoint($s-screen)
              padding: 0 4rem
            .wrap
              display: flex
              flex-flow: row nowrap
              justify-content: space-between
              align-items: center
              column-gap: 2rem
              width: 100%
              @include breakpoint($s-screen)
                overflow: hidden
              .hover-star
                width: 60px
                opacity: 0
                @include breakpoint($m-screen)
                  display: none
              span
                width: calc(100% - 33px - 2rem)
                @include breakpoint($s-screen)
                  overflow-wrap: break-word
                  width: 100%
            .arrow-tr
              transition: all 0.3s ease
              width: 33px
              @include breakpoint($m-screen)
                  margin-left: 2rem
        &:hover
          background-color: white
          a *
            color: #1D1D1D
          .big-wrap
            .wrap
              .hover-star
                opacity: 1
            .arrow-tr
              filter: invert(100%)
              width: 44px  
      .separator
        width: 90%
        height: 1px
        margin-right: auto
        margin-left: auto
        background-color: #313131
        @include breakpoint($s-screen)
          width: 100%
</style>