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
    eta: '3',
  },
  {
    name: 'car2',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '5',
  },
  {
    name: 'car3',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '9',
  },
  {
    name: 'car4',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '17',
  },
  {
    name: 'car5',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '19',
  },
  {
    name: 'car6',
    type: 'Medicinal Transportation',
    battery: '40',
    eta: '25',
  },
  {
    name: 'car7',
    type: 'Medicinal Transportation',
    battery: '40',
    eta: '37',
  },
  {
    name: 'car8',
    type: 'Goods Transportation',
    battery: '40',
    eta: '38',
  },
  {
    name: 'car9',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '40',
  },
  {
    name: 'car10',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '44',
  },
  {
    name: 'car11',
    type: 'Goods Transportation',
    battery: '40',
    eta: '43',
  },
  {
    name: 'car12',
    type: 'Goods Transportation',
    battery: '40',
    eta: '48',
  },
  {
    name: 'car13',
    type: 'Goods Transportation',
    battery: '40',
    eta: '50',
  },
  {
    name: 'car14',
    type: 'Goods Transportation',
    battery: '40',
    eta: '55',
  },
  {
    name: 'car15',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '70',
  },
  {
    name: 'car16',
    type: 'Goods Transportation',
    battery: '40',
    eta: '74',
  },
  {
    name: 'car17',
    type: 'Goods Transportation',
    battery: '40',
    eta: '81',
  },
  {
    name: 'car18',
    type: 'Passenger Transportation',
    battery: '40',
    eta: '82',
  },
  {
    name: 'car1',
    type: 'Goods Transportation',
    battery: '40',
    eta: '84',
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
      <va-scroll-container style="max-height: 52rem" vertical>
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
            <va-list-item-label class="listtext">
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

.listtext {
  font-size: 14px;
}
</style>
