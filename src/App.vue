<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'

let show_menu = ref(false)
function onOpenMenu(el, done) {
  document.body.classList.add('menu-displayed')
}
function onCloseMenu(el, done) {
  document.body.classList.remove('menu-displayed')
}
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">
        <div class="logo">
          <img alt="Vue logo" class="logo" src="@/assets/images/logo.svg"/>
          <span>théo<br>renaux</span>
        </div>
      </RouterLink>

      <button @click="show_menu = !show_menu">
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
    <Transition name="fade" @before-enter="onOpenMenu" @after-leave="onCloseMenu" appear>
      <div v-if="show_menu" class="fs_links">
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/">ui/ux design</RouterLink>
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/about">graphisme</RouterLink>
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/about">photographie</RouterLink>
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/about">mes projets</RouterLink>
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/about">à propos</RouterLink>
        <hr>
        <RouterLink @click="show_menu = !show_menu" to="/about">me contacter</RouterLink>
        <hr>
      </div>
    </Transition>
  </header>

  <Transition name="fade">
    <RouterView />
  </Transition>
</template>

<style lang="sass" scoped>
  @import "@/assets/styles/breakpoints.sass"

  .fade-enter-active, .fade-leave-active
    transition: opacity 0.3s ease
  .fade-enter-from, .fade-leave-to
    opacity: 0

  header
    position: fixed
    max-width: 1920px
    width: 100%
    padding: 2rem 4.5rem
    backdrop-filter: blur(10px)
    background-color: #101010CC
    border-radius: 0 0 10px 10px
    z-index: 99
    @include breakpoint($s-screen)
      padding: 15px
      background-color: rgba(12, 12, 12, 0.8)

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
        width: 40px
        > span
          display: none

    button
      width: 40px
      height: 40px
      background-color: #282828
      border-radius: 17px
      display: none
      transition: all 0.3s ease
      @include breakpoint($s-screen)
        display: flex
        justify-content: center
        align-items: center
      .circles
        display: grid
        grid-template-columns: repeat(2, 1fr)
        grid-template-rows: repeat(2, 1fr)
        grid-gap: 6px
      
        span
          width: 10px
          height: 10px
          border-radius: 10px
          background-color: white
          transition: all 0.3s ease
          animation: 0.1s forwards
          animation-iteration-count: 1
          animation-name: circles_btn_out

          &:nth-child(4n + 3)
            background-color: #7e7e7e

        @keyframes circles_btn
          0%
            transform: scale(1)
          90%
            transform: scale(1.6)
          100%
            transform: scale(1.3)

        @keyframes circles_btn_out
          0%
            transform: scale(1.3)
          100%
            transform: scale(1)

      &:hover, &:active //TODO
        background-color: #3e3e3e
        span
          animation-name: circles_btn

          &:nth-child(4n + 2)
            animation-delay: 0.05s
          &:nth-child(4n + 3)
            animation-delay: 0.1s
            background-color: #7e7e7e
          &:nth-child(4n + 4)
            animation-delay: 0.15s
          
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

  .fs_links
    display: none
    z-index: 15
    @include breakpoint($s-screen)
      position: absolute
      top: 70px
      left: 0
      display: flex
      flex-flow: column nowrap
      justify-content: space-between
      align-items: center
      row-gap: 1.5rem
      width: 100%
      height: calc( 100vh - 70px )
      overflow-y: scroll
      background-color: rgba(16, 16, 16, 0.5)
      backdrop-filter: blur(20px)

      a
        position: relative
        color: white
        text-decoration: none
        text-transform: uppercase

      hr
        margin: 0
        width: calc( 100vw - 100px )
        min-height: 1px
        background-color: #313131
        border: none

        &:first-child
          margin-top: 2rem
        &:last-child
          margin-bottom: 2rem
</style>
