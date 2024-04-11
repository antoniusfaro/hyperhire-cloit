<template>
  <q-card class="my-card no-box-shadow">
    <q-card-section>
      <div>
        <div
          class="icon-wrapper text-blue-grey-13 bg-grey-3 q-pa-sm rounded-borders q-mb-sm"
        >
          <img
            :src="icon"
            :alt="title"
            width="24"
            height="24"
            class="q-ma-none"
          />
        </div>

        <span class="block text-body2 text-weight-bolder q-mb-md">{{
          title
        }}</span>

        <div class="footer-link cursor-pointer">
          <a :href="link" class="text-weight-bolder text-grey-7">
            <span> 바로가기 </span>
            <img
              width="16"
              height="16"
              src="/src/assets/icons/footer/right-arrow.png"
              alt="Right Arrow Link Icon"
          /></a>
        </div>
      </div>
    </q-card-section>
  </q-card>
</template>

<script setup lang="ts">
defineOptions({
  name: 'FooterCard',
});

export interface FooterCardProps {
  title: string;
  link: string;
  icon: string;
}

withDefaults(defineProps<FooterCardProps>(), {
  title: '해외 개발자 원격 채용',
  link: '#',
  icon: '/src/assets/icons/footer/avatar.png',
});
</script>

<style>
.icon-wrapper {
  display: flex;
  width: fit-content;
}
.footer-link {
  & a {
    display: flex;
    align-items: center;
    gap: 0.25rem;
    text-decoration: none !important;
  }
}
</style>
