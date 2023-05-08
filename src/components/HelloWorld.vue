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
      minimized: false,
    };
  },
};
</script>

<template>
  <div style="height: 100%">
    <div class="searcch_and_x">
    <va-list-item width="21rem">
      <va-list-item-section>
        <va-input v-model="value" class="mb-6" placeholder="Search for a car" />
      </va-list-item-section>
      <va-list-item-section icon>
        <va-checkbox
          v-model="minimized"
          class="mt-2"
          color="#9c27b0"
          checked-icon="X"
        />
      </va-list-item-section>
    </va-list-item>
    <va-list-separator spaced="true"> </va-list-separator>
    </div>
      <va-sidebar :minimized="minimized" width="21rem" minimized-width="10px">
      <va-scroll-container style="max-height: 45rem" vertical >
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
        </va-scroll-container>
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
.search_and_X {
  height: 10%; 
  background-color: #1a1a1a; 
  padding-top: 2rem; 
  padding-bottom: 2rem;
}
</style>
