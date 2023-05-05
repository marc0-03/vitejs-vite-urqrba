<script setup>
import { ref } from 'vue';

defineProps({
  msg: String,
});

const count = ref(0);
const cars = [
  {
    name: "car1",
    type: "Goods Transportation",
    battery: "40",
    eta: "17",
  },
];
</script>

<template>
  <va-scroll-container style="max-height: 400px" vertical>
    <va-list>
      <va-list-item v-for="car in cars" :key="index" class="list__item">
        <va-list-item-section icon>
          <img src="../assets/Truck.png" height="30">
        </va-list-item-section>
        <va-list-item-section>
          <va-list-item-label>
            {{ car.name }}
          </va-list-item-label>
          <va-list-item-label caption>
            {{ car.type }}
          </va-list-item-label>
        </va-list-item-section>
        <va-list-item-section icon>
          <img src="../assets/Battery.png" height="30">
        </va-list-item-section>
      </va-list-item>
    </va-list>
  </va-scroll-container>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>
</template>

<style lang="scss" scoped>
.list__item + .list__item {
  margin-top: 20px;
}
.va-icon + .va-icon {
  margin-left: 2rem;
}
</style>
