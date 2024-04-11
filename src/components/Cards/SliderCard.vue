<template>
  <q-card class="my-card no-box-shadow">
    <q-card-section>
      <div>
        <div
          class="text-blue-grey-13 bg-grey-3 q-pa-sm rounded-borders q-mb-sm"
          style="display: inline-block"
        >
          <q-icon :size="'sm'" name="code" />
        </div>

        <span class="block text-body2 text-weight-bolder q-mb-md"
          >해외 개발자 원격 채용</span
        >

        <div class="row cursor-pointer">
          <a href="http://" class="text-weight-bolder text-grey-7">
            바로가기
          </a>
        </div>
      </div>
    </q-card-section>
  </q-card>
</template>

<script setup lang="ts">
defineOptions({
  name: 'SliderCard',
});

export interface SliderCardProps {
  //   title: string;
  caption?: string;
  link?: string;
  icon?: string;
}

withDefaults(defineProps<SliderCardProps>(), {
  caption: '',
  link: '#',
  icon: '',
});
</script>
