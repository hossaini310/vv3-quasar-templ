<template>
  <q-header class="bg-primary text-white" height-hint="98">
    <q-toolbar>
      <q-btn dense flat round icon="r_menu" @click="$emit('toggleLeftDrawer')" />

      <q-toolbar-title>
        <q-avatar class="rotate-on-hover">
          <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
        </q-avatar>
        <span class="q-ml-sm"> vv3-templ-quasar </span>
      </q-toolbar-title>
    </q-toolbar>

    <q-tabs align="left">
      <q-route-tab to="/" label="Home" />
      <q-route-tab to="/about" label="About" />
    </q-tabs>
  </q-header>
</template>

<script setup>
defineEmits(['toggleLeftDrawer']);
</script>

<style scoped>
.rotate-on-hover {
  transform: rotate(0);
  transition: transform 0.8s ease-in-out;
}
.rotate-on-hover:hover {
  transform: rotate(-360deg);
  transition: transform 0.8s ease-in-out;
}
</style>
