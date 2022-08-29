<template>
    <div>
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1980"
        img-height="980"
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
  
  
        <b-carousel-slide img-src="https://picsum.photos/1980/1020/?image=58" style="height:100vh !important"></b-carousel-slide>
        <b-carousel-slide img-src="https://picsum.photos/1980/1020/?image=58" style="height:100vh !important"></b-carousel-slide>
        <b-carousel-slide img-src="https://picsum.photos/1980/1020/?image=58" style="height:100vh !important"></b-carousel-slide>
        <b-carousel-slide img-src="https://picsum.photos/1980/1020/?image=58" style="height:100vh !important"></b-carousel-slide>
  


      </b-carousel>
    </div>
  </template>
  
  <script>
    export default {
      data() {
        return {
          slide: 0,
          sliding: null
        }
      },
      methods: {
        onSlideStart(slide) {
          this.sliding = true
        },
        onSlideEnd(slide) {
          this.sliding = false
        }
      }
    }
  </script>
  <style>
    .carousel-1{
        z-index: 1;
    }
  </style>