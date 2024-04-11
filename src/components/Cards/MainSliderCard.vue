<template>
  <q-card
    class="slider-card row justify-start items-center no-box-shadow q-pa-md"
  >
    <q-avatar square size="56" class="slider-card-avatar">
      <img
        :src="icon"
        :alt="title"
        class="slider-card-avatar-img"
        width="36px"
        height="36px"
      />
    </q-avatar>
    <q-item-label class="text-h5 text-weight-bolder">{{ title }}</q-item-label>
  </q-card>
</template>

<script setup lang="ts">
defineOptions({
  name: 'MainSliderCard',
});

export interface MainSliderCardProps {
  title: string;
  icon: string;
}

withDefaults(defineProps<MainSliderCardProps>(), {
  title: '해외 마케팅',
  icon: '/src/assets/icons/slider/icon-marketing.png',
});
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
    &-img {
      width: 32px !important;
      height: 32px !important;
    }
  }
}
</style>
