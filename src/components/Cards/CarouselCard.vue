<template>
  <q-card
    class="carousel-card cursor-pointer no-box-shadow rounded-borders q-pa-lg row items-center justify-center"
  >
    <q-avatar size="120px" class="avatar q-mb-md">
      <img :src="img" />
      <q-badge floating class="avatar-badge" color="blue">
        <img
          :src="`/src/assets/images/national-flags/${nationality}-flag.png`"
          alt="Venezuela National Flag"
        />
      </q-badge>
    </q-avatar>

    <span
      class="card-title block text-h5 text-weight-bolder text-black text-center"
      >{{ name }}</span
    >
    <span
      class="card-subtitle block text-subtitle1 text-weight-bolder text-blue-13 text-center q-mb-lg"
      >{{ occupation }} · {{ yoe }}</span
    >

    <div
      class="card-specs row items-center justify-center q-gutter-xs text-weight-bolder text-grey-14"
    >
      <span class="user-item" v-for="(s, index) in specialities" :key="index">{{
        s
      }}</span>
    </div>
  </q-card>
</template>

<script setup lang="ts">
defineOptions({
  name: 'CarouselCard',
});

export interface CarouselCardProps {
  name: string;
  nationality: string;
  occupation: string;
  yoe: string;
  img: string;
  specialities: string[];
}

withDefaults(defineProps<CarouselCardProps>(), {
  name: 'Abhishek Gupta',
  nationality: 'venezuela',
  occupation: 'None',
  yoe: '0yr',
  img: 'https://cdn.quasar.dev/img/avatar2.jpg',
  specialities: () => ['Speciality A', 'Speciality B', 'Speciality C'],
});
</script>

<style lang="scss" scoped>
.carousel-card {
  width: 292px;
  @media (max-width: $breakpoint-md-max) {
    width: 292px;
    height: 385px;
  }
  @media (max-width: $breakpoint-xs-max) {
    width: 234px;
    height: 311px;
    padding: 24px 16px;
    .avatar {
      width: 80px;
      height: 80px;
    }
  }
  padding: 32px;
  border-radius: 12px;

  .avatar {
    border-radius: 60px !important;
    &-badge {
      top: initial;
      bottom: 5px;
      right: 5px;
      width: 25px;
      height: 18px;
      padding: 0 !important;
    }
  }

  .user-item {
    padding: 4px 12px;
    border-radius: 6px;
    border: 1px solid #c1c5cf;
  }

  .card-title {
    @media (max-width: $breakpoint-md-max) {
      font-size: 24px;
    }
    @media (max-width: $breakpoint-xs-max) {
      font-size: 18px;
      margin-bottom: 0;
    }
  }

  .card-subtitle {
    @media (max-width: $breakpoint-md-max) {
      font-size: 18px;
    }
    @media (max-width: $breakpoint-xs-max) {
      font-size: 14px;
      margin-bottom: 0;
    }
  }

  .card-specs {
    @media (max-width: $breakpoint-md-max) {
      font-size: 14px;
    }
    @media (max-width: $breakpoint-xs-max) {
      font-size: 12px;
    }
  }
}
</style>
