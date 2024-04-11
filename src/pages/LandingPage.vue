<template>
  <div class="text-white main">
    <div class="main q-pa-xl main-section">
      <div class="row q-mt-xl">
        <div class="col-xs-12 col-md-6">
          <transition
            appear
            enter-active-class="animated delay-1s fadeIn slower"
            leave-active-class="animated fadeOut"
          >
            <img
              src="/src/assets/images/bubbles/main-bubble.png"
              alt="Main Bubble"
              height="39"
              class="q-mt-md"
            />
          </transition>
          <transition
            appear
            enter-active-class="animated fadeIn slower"
            leave-active-class="animated fadeOut"
          >
            <h1
              class="main-heading text-h3 text-weight-bolder text-white q-mt-0"
            >
              <span>
                최고의 실력<span class="text-white-90">을 가진</span>
              </span>
              <span class="block">
                외국인 인재<span class="text-white-90"
                  >를 찾고 계신가요?
                </span></span
              >
            </h1>
          </transition>
          <transition
            appear
            enter-active-class="animated delay-1s fadeIn slower"
            leave-active-class="animated fadeOut"
          >
            <h2 class="text-h5 text-weight-bolder text-white-90">
              <span> 법률 및 인사관리 부담없이 </span>
              <span class="block"> 1주일 이내에 원격으로 채용해보세요. </span>
            </h2>
          </transition>
          <transition
            appear
            enter-active-class="animated delay-1s fadeIn slower"
            leave-active-class="animated fadeOut"
          >
            <h2
              class="text-h6 text-weight-bolder text-white text-underline q-mb-xl"
            >
              개발자가 필요하신가요?
            </h2>
          </transition>

          <div class="row justify-between desktop-only">
            <transition
              appear
              enter-active-class="animated fadeIn slower"
              leave-active-class="animated fadeOut"
            >
              <div class="section-wrapper">
                <span class="block text-h6 text-weight-bolder q-mb-md"
                  >평균 월 120만원</span
                >
                <span class="block text-white-90">
                  임금을 해당 국가를 기준
                </span>
                <span class="block text-white-90"> 으로 계산합니다. </span>
              </div>
            </transition>
            <transition
              appear
              enter-active-class="animated fadeIn slower"
              leave-active-class="animated fadeOut"
            >
              <div class="section-wrapper">
                <span class="block text-h6 text-weight-bolder q-mb-md"
                  >최대 3회 인력교체</span
                >
                <span class="block text-white-90">
                  막상 채용해보니 맞지 않</span
                >
                <span class="block text-white-90">아도 걱정하지 마세요.</span>
              </div>
            </transition>
            <transition
              appear
              enter-active-class="animated fadeIn slower"
              leave-active-class="animated fadeOut"
            >
              <div class="section-wrapper">
                <span class="block text-h6 text-weight-bolder q-mb-md"
                  >평균 3일, 최대 10일</span
                >
                <span class="block text-white-90">급하게 사람이 필요한 경</span>
                <span class="block text-white-90"
                  >우에도 빠른 채용이 가능합니다.</span
                >
              </div>
            </transition>
          </div>
        </div>
        <div class="col-xs-12 col-md-6 row align-center justify-center q-py-xl">
          <transition
            appear
            enter-active-class="animated delay-1s fadeIn slower"
            leave-active-class="animated fadeOut"
          >
            <img
              src="/src/assets/images/bubbles/card-bubble.png"
              alt="Card Bubble"
              height="51"
            />
          </transition>
          <carousel-3d
            :width="234"
            :height="385"
            :border="0"
            :controlsVisible="true"
            class="mobile-only"
          >
            <slide
              v-for="(user, index) in userCarousel"
              :key="user.name"
              :index="index"
              style="background: transparent; color: white"
            >
              <CarouselCard v-bind="user" />
            </slide>
          </carousel-3d>
          <carousel-3d
            :width="292"
            :height="385"
            :border="0"
            :controlsVisible="true"
            class="desktop-only"
          >
            <slide
              v-for="(user, index) in userCarousel"
              :key="user.name"
              :index="index"
              style="background: transparent; color: white"
            >
              <CarouselCard v-bind="user" />
            </slide>
          </carousel-3d>
        </div>
      </div>
      <div class="desktop-only">
        <HomeSlider />
      </div>
    </div>
    <div class="footer text-black q-pa-xl">
      <div class="row">
        <div class="col-xs-12 col-md-4 q-mb-lg">
          <img
            src="../assets/images/hyperhire-logo-fc.png"
            alt=""
            :height="34"
            :width="187"
          />
          <span
            class="block text-body2 text-weight-bolder text-grey-10 q-mt-sm"
          >
            우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
          </span>
          <span
            class="block text-body2 text-weight-bolder text-grey-14 q-mt-sm"
          >
            010-0000-0000
          </span>
          <span
            class="block text-body2 text-weight-bolder text-grey-14 q-mt-sm"
          >
            aaaaa@naver.com
          </span>
        </div>
        <div class="col-xs-12 col-md-8">
          <div class="row q-gutter-md">
            <FooterCard
              v-for="(footer, index) in footerCard"
              :key="index"
              v-bind:="footer"
            />
          </div>
        </div>
      </div>
      <div class="row q-mt-xl">
        <div class="col-xs-12 col-md-4">
          <div class="row q-mb-lg">
            <div class="col-8">
              <span
                class="block text-body2 text-weight-bolder text-grey-10 q-mb-md"
              >
                상호명
              </span>
              <span
                class="block text-body2 text-weight-bolder text-grey-14 q-mb-sm"
              >
                하이퍼하이어
              </span>
              <span class="block text-body2 text-weight-bolder text-grey-14">
                Hyperhire India Private Limited
              </span>
            </div>
            <div class="col-4">
              <span
                class="block text-body2 text-weight-bolder text-grey-10 q-mb-md"
              >
                대표 CEO
              </span>
              <span
                class="block text-body2 text-weight-bolder text-grey-10 q-mb-sm"
              >
                김주현
              </span>
              <span class="block text-body2 text-weight-bolder text-grey-14">
                Juhyun Kim
              </span>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-md-8">
          <div class="row">
            <div class="col-xs-12 col-md-4 q-mb-xl">
              <span
                class="block text-body2 text-weight-bolder text-grey-10 q-mb-md"
              >
                사업자등록번호 CIN
              </span>
              <span
                class="block text-body2 text-weight-bolder text-grey-14 q-mb-sm"
              >
                427-86-01187
              </span>
              <span class="block text-body2 text-weight-bolder text-grey-14">
                U74110DL2016PTC290812
              </span>
            </div>
            <div class="col-xs-12 col-md-8 q-mb-xl">
              <span
                class="block text-body2 text-weight-bolder text-grey-10 q-mb-md"
              >
                주소 ADDRESS
              </span>
              <span
                class="block text-body2 text-weight-bolder text-grey-14 q-mb-sm"
              >
                서울특별시 강남대로 479, 지하 1층 238호
              </span>
              <span class="block text-body2 text-weight-bolder text-grey-14">
                D-138, Street number 11, Jagjeet Nagar, North East Delhi, New
                Delhi, 110053 India
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="row q-mb-lg">
        <span class="text-weight-bolder text-grey-14">ⓒ 2023 Hyperhire</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import FooterCard, {
  FooterCardProps,
} from 'src/components/Cards/FooterCard.vue';
import CarouselCard, {
  CarouselCardProps,
} from '../components/Cards/CarouselCard.vue';
import { Carousel3d, Slide } from 'vue3-carousel-3d';
import 'vue3-carousel-3d/dist/index.css';
import HomeSlider from 'src/components/Sliders/HomeSlider.vue';

defineOptions({
  name: 'LandingPage',
  components: {
    Carousel3d,
    Slide,
  },
  mounted() {
    const prev = document.querySelectorAll('.prev');
    const next = document.querySelectorAll('.next');
    if (prev) {
      prev[0].classList.add('text-white');
      prev[1].classList.add('text-white');
    }
    if (next) {
      next[0].classList.add('text-white');
      next[1].classList.add('text-white');
    }
  },
});

const userCarousel: CarouselCardProps[] = [
  {
    name: 'Abhishek Gupta',
    nationality: 'venezuela',
    occupation: '마케팅',
    yoe: '2y+',
    img: '../src/assets/images/users/user-dummy.png',
    specialities: [
      '마케팅 콘텐츠 제작',
      '인스타그램 관리',
      '트위터 관리',
      '블로그 글 작성',
    ],
  },
  {
    name: 'Abhishek Gupta',
    nationality: 'venezuela',
    occupation: '마케팅',
    yoe: '2y+',
    img: '../src/assets/images/users/user-dummy.png',
    specialities: [
      '마케팅 콘텐츠 제작',
      '인스타그램 관리',
      '트위터 관리',
      '블로그 글 작성',
    ],
  },
  {
    name: 'Abhishek Gupta',
    nationality: 'venezuela',
    occupation: '마케팅',
    yoe: '2y+',
    img: '../src/assets/images/users/user-dummy.png',
    specialities: [
      '마케팅 콘텐츠 제작',
      '인스타그램 관리',
      '트위터 관리',
      '블로그 글 작성',
    ],
  },
];

const footerCard: FooterCardProps[] = [
  {
    title: '해외 개발자 원격 채용',
    link: '#',
    icon: '../src/assets/icons/footer/icon-code.png',
  },
  {
    title: '외국인 원격 채용 (비개발)',
    link: '#',
    icon: '../src/assets/icons/footer/icon-avatar.png',
  },
  {
    title: '한국어 가능 외국인 채용',
    link: '#',
    icon: '../src/assets/icons/footer/icon-kor.png',
  },
  {
    title: '해외 개발자 활용 서비스',
    link: '#',
    icon: '../src/assets/icons/footer/icon-gear.png',
  },
];
</script>

<style lang="scss" scoped>
.main {
  margin-top: -50px;
  background-image: url('/src/assets/images/background-2.png');
  background-blend-mode: color-burn;
  background-size: cover;
  background-position: center 10px;
  background-repeat: no-repeat;
  overflow: hidden;

  &-heading {
    margin-top: 8px !important;
    @media (max-width: $breakpoint-xs-max) {
      font-size: 48px;
      height: 120vh !important;
    }
    @media (max-width: $breakpoint-xs-max) {
      font-size: 36px;
      height: auto !important;
    }
  }
}

.main-section {
  @media (max-width: $breakpoint-xs-max) {
    padding: 48px;
  }
  @media (max-width: $breakpoint-xs-max) {
    padding: 24px;
  }
}

.footer {
  background-color: #fbfbfb;
  @media (max-width: $breakpoint-xs-max) {
    padding: 48px;
  }
  @media (max-width: $breakpoint-xs-max) {
    padding: 24px;
  }
}

.text-white-90 {
  color: rgba(255, 255, 255, 0.9);
}

.text-underline {
  text-decoration: underline;
}

.section-wrapper {
  padding-top: 8px;
  border-top: 1px solid #ffffff;
}

.carousel-3d-controls .prev,
.carousel-3d-controls .prev {
  background-color: red;
  background-color: red;
  color: #ffffff !important;
}
.carousel-3d-slide.left-1 {
  transform: translateX(-194px) translateZ(-400px) rotateY(0) !important;
}
.carousel-3d-slide.left-2 {
  transform: translateX(-389px) translateZ(-500px) rotateY(0) !important;
}
.carousel-3d-slide.right-1 {
  transform: translateX(194px) translateZ(-400px) rotateY(0) !important;
}
.carousel-3d-slide.right-2 {
  transform: translateX(389px) translateZ(-500px) rotateY(0) !important;
}
</style>
