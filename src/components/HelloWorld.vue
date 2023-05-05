<script setup>
import { ref } from 'vue';

defineProps({
  msg: String,
});

const count = ref(0);
const cars = [
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
  },
];
</script>
<script>
export default {
  data() {
    return {
      items: [
        { title: 'Dashboard', icon: 'dashboard' },
        { title: 'Sidebar demo', icon: 'room', active: true },
        { title: 'Loop', icon: 'loop' },
      ],
      minimized: false,
    };
  },
};
</script>

<template>
  <div style="height: 48rem">
    <va-list-item-section icon>
      <va-checkbox v-model="minimized" class="mt-2" label="Minimized" />
    </va-list-item-section>
    <va-list-item>
      <va-list-item-section>
        <va-input v-model="value" class="mb-6" placeholder="Placeholder" />
      </va-list-item-section>
    </va-list-item>
    <va-sidebar :minimized="minimized" width="21rem" minimized-width="64px">
      <va-list-item v-for="car in cars" :key="index" class="list__item">
        <va-list-item-section icon>
          <img src="../assets/Truck.png" height="30" />
        </va-list-item-section>
        <va-list-item-section>
          <va-list-item-label>
            {{ car.name }} - {{ car.type }}
          </va-list-item-label>
          <va-list-item-label caption>
            ETA: {{ car.eta }} min - Battery {{ car.battery }}%
          </va-list-item-label>
        </va-list-item-section>
        <va-list-item-section icon>
          <img src="../assets/Battery.png" height="30" />
        </va-list-item-section>
      </va-list-item>
    </va-sidebar>
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
