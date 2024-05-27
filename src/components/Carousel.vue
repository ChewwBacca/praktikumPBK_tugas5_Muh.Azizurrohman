<template>
    <q-carousel
      animated
      v-model="slide"
      infinite
      navigation
      arrows
      :autoplay="5000"
    >
      <q-carousel-slide
        v-for="(image, index) in images"
        :name="index"
        :img-src="image.src"
        key="index"
      >
        <!-- Caption untuk setiap gambar -->
        <div class="caption">{{ image.caption }}</div>
      </q-carousel-slide>
    </q-carousel>
  </template>
  
  <script>
  export default {
    name: 'MyCarousel',
    data() {
      return {
        slide: 0,
        images: [
          {
            src: 'https://images.unsplash.com/photo-1627560270549-5c77fcde0ed3?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          },
          {
            src: 'https://images.unsplash.com/photo-1640955014216-75201056c829?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          },
          {
            src: 'https://images.unsplash.com/photo-1630794180018-433d915c34ac?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          },
          {
            src: 'https://images.unsplash.com/photo-1542039375-28138150cc31?q=80&w=2074&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
          },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .q-carousel {
    /* Responsive design adjustments */
    max-width: 10000px;
    height: 500px;
    position: relative; /* Changed from absolute for better responsiveness */
  }
  
  .q-carousel-slide {
    /* Visual enhancements */
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .caption {
    /* Accessibility and design improvements */
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(0, 0, 0, 0.7); /* Slightly darker for better readability */
    color: #fff;
    padding: 10px;
    border-radius: 10px;
    font-size: 20px; /* Adjusted for better mobile readability */
  }
  </style>