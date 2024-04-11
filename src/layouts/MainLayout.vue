<template>
  <q-layout view="hHh lpR fFf">
    <q-header
      reveal
      elevated
      class="my-header bg-transparent text-white no-box-shadow q-px-xl z-max"
    >
      <q-toolbar class="q-px-none">
        <img
          src="/src/assets/images/hyperhire-logo-white.png"
          alt="Hyperhire Logo White"
          height="24"
        />
        <q-space></q-space>
        <div class="desktop-only row items-center">
          <DropdownButton />
          <span class="text-weight-bolder">해외 개발자 활용 서비스</span>
        </div>
        <q-space></q-space>
        <q-btn flat round dense icon="menu" class="q-mr-sm mobile-only" />
        <q-btn
          color="white"
          text-color="black"
          label="문의하기"
          class="my-button desktop-only no-box-shadow text-weight-bolder q-px-lg"
        />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import DropdownButton from 'src/components/DropdownButton.vue';

defineOptions({
  name: 'MainLayout',
});
</script>

<style lang="scss">
.my-header {
  box-shadow: none !important;
  @media (max-width: $breakpoint-xs-max) {
    padding-left: 48px;
    padding-right: 48px;
  }
  @media (max-width: $breakpoint-xs-max) {
    padding-left: 24px;
    padding-right: 24px;
  }
}
.my-button,
.q-layout__shadow::after {
  box-shadow: none !important;
}

.my-button {
  color: #4a77ff !important;
  border-radius: 8px;
  &::before {
    box-shadow: none !important;
  }
}
</style>
