<script setup>
  import { Fancybox } from "@fancyapps/ui";
  import { Carousel } from "@fancyapps/ui/dist/carousel/carousel.esm.js";
  import "@fancyapps/ui/dist/fancybox/fancybox.css"
  import "@fancyapps/ui/dist/carousel/carousel.css";
  import { onMounted } from 'vue'

  onMounted(() => {
    Fancybox.bind("[data-fancybox]", {});
    const container = document.getElementById("myCarousel");
    const options = {
      Dots: false,
      Navigation: false,
      infinite: false,
      slidesPerPage: 1,
      preload: 1,
      center: true,
    };
    new Carousel(container, options);
  })
</script>

<template>
  <div class="f-carousel" id="myCarousel">
    <div class="f-carousel__viewport">
      <div class="f-carousel__track">
        <div class="f-carousel__slide" data-fancybox="a" data-src="/src/components/projects/malongo/assets/image-1.png"><img src="@/components/projects/malongo/assets/image-1.png" alt=""></div>
        <div class="f-carousel__slide" data-fancybox="a" data-src="/src/components/projects/malongo/assets/image-2.png"><img src="@/components/projects/malongo/assets/image-2.png" alt=""></div>
        <div class="f-carousel__slide" data-fancybox="a" data-src="/src/components/projects/malongo/assets/image-1.png"><img src="@/components/projects/malongo/assets/image-1.png" alt=""></div>
        <div class="f-carousel__slide" data-fancybox="a" data-src="/src/components/projects/malongo/assets/image-2.png"><img src="@/components/projects/malongo/assets/image-2.png" alt=""></div>
        <div class="f-carousel__slide" data-fancybox="a" data-src="/src/components/projects/malongo/assets/image-1.png"><img src="@/components/projects/malongo/assets/image-1.png" alt=""></div>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
  @import "@/assets/styles/breakpoints.sass"

  #myCarousel
    position: relative
    width: 100%
    --f-carousel-slide-height: 300px
    --f-carousel-spacing: 20px

    .f-carousel__slide
      width: auto
      display: flex
      justify-content: center !important
      align-items: center !important
      @include breakpoint($s-screen)
        width: 60%
      &:first-child
        &::before
          content: ''
          position: relative
          display: inline-block
          width: 80px
          min-width: 80px
          height: 300px
          @include breakpoint($s-screen)
            width: 20px
            min-width: 20px
      &:last-child
        &::after
          content: ''
          position: relative
          display: block
          width: 80px
          min-width: 80px
          height: 300px
          @include breakpoint($s-screen)
            width: 20px
            min-width: 20px
      img
        height: 100%
        width: 100%
        border-radius: 10px
        @include breakpoint($s-screen)
          object-fit: cover
    &::after
      content: ''
      position: absolute
      width: 100%
      height: 100%
      top: 0
      left: 50%
      transform: translateX(-50%)
      background: rgb(16,16,16)
      background: -moz-linear-gradient(90deg, rgba(16,16,16,1) 0%, rgba(0,0,0,0) 50%, rgba(16,16,16,1) 100%)
      background: -webkit-linear-gradient(90deg, rgba(16,16,16,1) 0%, rgba(0,0,0,0) 50%, rgba(16,16,16,1) 100%)
      background: linear-gradient(90deg, rgba(16,16,16,1) 0%, rgba(0,0,0,0) 50%, rgba(16,16,16,1) 100%)
      filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#101010",endColorstr="#101010",GradientType=1)
      pointer-events: none
      @include breakpoint($s-screen)
        //width: 200% // TODO blem fancybox
</style>