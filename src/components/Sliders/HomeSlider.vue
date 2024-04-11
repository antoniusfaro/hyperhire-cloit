<template>
  <div class="swiper q-mt-xl">
    <!-- Additional required wrapper -->

    <div class="swiper-wrapper" autoplay-delay="2500">
      <!-- Slides -->
      <!-- <div class="swiper-slide">Slide 1</div>
      <div class="swiper-slide">Slide 2</div>
      <div class="swiper-slide">Slide 3</div> -->
      <div v-for="main in mainSlider" :key="main.title" class="swiper-slide">
        <MainSliderCard v-bind="main" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import MainSliderCard from '../Cards/MainSliderCard.vue';
import Swiper from 'swiper';
// import Swiper styles
import 'swiper/css';
import 'swiper/css/autoplay';

export default {
  setup() {
    return {
      slide: ref(1),
    };
  },
  components: {
    MainSliderCard,
  },
  data() {
    return {
      mainSlider: [
        {
          title: '해외 마케팅',
          icon: '/src/assets/icons/slider/icon-marketing.png',
        },
        {
          title: '퍼블리셔',
          icon: '/src/assets/icons/slider/icon-image.png',
        },
        {
          title: '캐드원(제도사)',
          icon: '/src/assets/icons/slider/icon-box.png',
        },
        {
          title: '해외 세일즈',
          icon: '/src/assets/icons/slider/icon-target.png',
        },
        {
          title: '해외 CS',
          icon: '/src/assets/icons/slider/icon-call.png',
        },
      ],
    };
  },
  mounted() {
    const swiper = new Swiper('.swiper', {
      // Optional parameters
      direction: 'horizontal',
      loop: true,
      effect: 'fade',
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      // spaceBetween: 16,
      slidesPerView: '3',
      breakpoints: {
        320: {
          slidesPerView: 1,
          spaceBetween: 20,
        },
        480: {
          slidesPerView: 2,
          spaceBetween: 16,
        },
        640: {
          slidesPerView: 3,
          spaceBetween: 16,
        },
        1560: {
          slidesPerView: 4,
          spaceBetween: 16,
        },
      },

      // If we need pagination
      pagination: {
        el: '.swiper-pagination',
      },

      // Navigation arrows
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },

      // And if we need scrollbar
      scrollbar: {
        el: '.swiper-scrollbar',
      },
    });
    setInterval(() => {
      swiper.slideNext();
    }, 5000);
  },
};
</script>

<style lang="scss" scoped>
.slider-card {
  display: flex;
  width: 332px;
  gap: 1rem;
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 12px;
  &-avatar {
    background-color: rgba(255, 255, 255, 0.4);
    border-bottom-left-radius: 8px !important;
    border-bottom-right-radius: 8px !important;
  }
}
</style>
