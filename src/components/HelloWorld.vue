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
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Truck.png',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '17',
    src: '../assets/Medic.png',
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
    <div class="search_and_X">
      <va-list-item width="21rem">
        <va-list-item-section>
          <va-input
            v-model="value"
            class="mb-6"
            placeholder="Search for a car"
          />
        </va-list-item-section>
        <va-list-item-section icon>
          <va-checkbox
            v-model="minimized"
            class="mt-2"
            color="var(--va-text-primary)"
            checked-icon="X"
          />
        </va-list-item-section>
      </va-list-item>
    </div>
    <va-sidebar :minimized="minimized" width="21rem" minimized-width="64px">
      <va-scroll-container style="max-height: 47rem" vertical>
        <va-list-item v-for="car in cars" :key="index" class="list__item">
          <va-list-item-section icon v-if="car.type == 'Goods Transportation'">
            <img src="../assets/Truck.png" height="30" />
          </va-list-item-section>

          <va-list-item-section
            icon
            v-if="car.type == 'Medicinal Transportation'"
          >
            <img src="../assets/Medic.png" height="30" />
          </va-list-item-section>

          <va-list-item-section
            icon
            v-if="car.type == 'Passenger Transportation'"
          >
            <img src="../assets/Car.png" height="30" />
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
  background-color: var(--va-text-primary);
  padding-top: 1rem;
  padding-bottom: 1rem;
  padding-left: 0.3rem;
  width: 21rem;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.55);
}
</style>
