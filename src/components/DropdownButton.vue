<template>
  <div class="">
    <q-btn-dropdown color="transparent" label="채용" class="my-dropdown">
      <q-list>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label class="font-weight-bolder">채용</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>해외 개발자 원격 채용</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>외국인 원격 채용 (비개발 직군)</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>한국어 가능 외국인 채용</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown>
  </div>
</template>

<script>
export default {
  setup() {
    return {
      onItemClick() {
        // console.log('Clicked on an Item')
      },
    };
  },
};
</script>

<style lang="scss">
.my-dropdown,
.my-dropdown::before,
.my-dropdown::after {
  box-shadow: none !important;
}
</style>
