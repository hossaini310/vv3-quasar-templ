<template>
  <div class="column justify-center items-center">
    <TitleComp title="Vue 3 with Vueite 4 & Quasar 2"></TitleComp>
    <div class="q-mb-xl text-center">
      <p>
        This project uses the Material Icons library (both the sharp and the rounded versions). If
        you want to use the rounded version you need to add r_ before the icon name.
      </p>
      <span>Examples:</span>
      <div>
        <div class="row justify-center">
          <div class="row justify-center q-mr-md">
            <q-icon name="auto_awesome" size="2.1rem"></q-icon>
            <span class="q-ml-md text-h6 text-weight-light">auto_awesome</span>
          </div>
          <div class="row justify-center">
            <q-icon name="r_auto_awesome" size="2.1rem"></q-icon>
            <span class="q-ml-md text-h6 text-weight-light">r_auto_awesome</span>
          </div>
        </div>
        <div class="row justify-center">
          <div class="row justify-center q-mr-md">
            <q-icon name="home" size="2.1rem"></q-icon>
            <span class="q-ml-md text-h6 text-weight-light">home</span>
          </div>
          <div class="row justify-center">
            <q-icon name="r_home" size="2.1rem"></q-icon>
            <span class="q-ml-md text-h6 text-weight-light">r_home</span>
          </div>
        </div>
      </div>
    </div>
    <q-btn
      @click="increaseCounter()"
      class="q-px-xl q-py-md"
      color="primary"
      rounded
      :label="`Counter: ${store.counter}`"
    >
    </q-btn>
  </div>
</template>

<script setup>
import TitleComp from '@/components/TitleComp.vue';
import useDefaultStore from '@/stores/defaultStore.js';

const store = useDefaultStore();

const increaseCounter = () => store.increaseCounter();
</script>
