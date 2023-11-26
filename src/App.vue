<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">
        <div class="logo">
          <img alt="Vue logo" class="logo" src="@/assets/logo.svg"/>
          <span>théo<br>renaux</span>
        </div>
      </RouterLink>

      <button>
        <div class="circles">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
        </div> 
      </button>

      <div class="links">
        <div class="col">
          <RouterLink to="/">ui/ux design</RouterLink>
          <RouterLink to="/about">graphisme</RouterLink>
          <RouterLink to="/about">photographie</RouterLink>
        </div>
        <div class="col">
          <RouterLink to="/about">mes projets</RouterLink>
          <RouterLink to="/about">à propos</RouterLink>
          <RouterLink to="/about">me contacter</RouterLink>
        </div>
      </div>
    </nav>
  </header>

  <RouterView />
</template>

<style lang="sass" scoped>
  @import "@/assets/breakpoints.sass"

  header
    padding: 1.5rem 2rem
    background-color: rgba(12, 12, 12, 0.8)
    backdrop-filter: blur(10px)
    
  nav
    display: flex
    flex-flow: row nowrap
    justify-content: space-between
    align-items: center

    a
      text-transform: uppercase
      color: white
      text-decoration: none
    
    .logo
      display: flex
      flex-flow: row nowrap
      justify-content: space-between
      align-items: center
      column-gap: 1rem
      font-size: 1.25rem
      @include breakpoint($s-screen)
        > span
          display: none

    button
      width: 50px
      height: 50px
      background-color: #282828
      border-radius: 22px
      display: none
      @include breakpoint($s-screen)
        display: flex
        justify-content: center
        align-items: center
      .circles
        display: grid
        grid-template-columns: repeat(2, 1fr)
        grid-template-rows: repeat(2, 1fr)
        grid-gap: 8px
      
        span
          width: 12px
          height: 12px
          border-radius: 10px
          background-color: white
          transition: all 0.3s ease
          animation: 0.1s both
          animation-iteration-count: 1
          

          &:nth-child(4n + 2)
            animation-delay: 0.05s
          &:nth-child(4n + 3)
            animation-delay: 0.1s
            background-color: #7e7e7e
          &:nth-child(4n + 4)
            animation-delay: 0.15s
        
        @keyframes circles_btn
          0%
            transform: scale(1)
          90%
            transform: scale(1.6)
          100%
            transform: scale(1.2)

      &:hover
        span
          animation-name: circles_btn
          
    .links
      display: flex
      flex-flow: row nowrap
      justify-content: space-between
      align-items: flex-start
      column-gap: 5rem
      @include breakpoint($s-screen)
          display: none

      .col
        display: flex
        flex-flow: column nowrap
        justify-content: flex-start
        align-items: flex-start
        row-gap: 0.5rem


</style>
