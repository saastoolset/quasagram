<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar>
        <q-toolbar-title> Quasagram </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-footer class="bg-white">
      <q-tabs active-color="primary" indicator-color="transparent" class="text-grey-10" v-model="tab">
        <q-route-tab icon="eva-home-outline" label="Home" name="home" to="/" />

        <q-route-tab icon="eva-camera-outline" label=" Camera" name="camera" to="/camera" />
      </q-tabs>
    </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  // setup() {
  //   const leftDrawerOpen = ref(false);

  //   return {
  //     // essentialLinks: linksList,
  //     // leftDrawerOpen,
  //     // toggleLeftDrawer() {
  //     //   leftDrawerOpen.value = !leftDrawerOpen.value;
  //     // },
  //   };
  // },
});
</script>

<style lang="sass">
  .q-toolbar__title
    text-align: center
  .q-foooter
    .q-tab__icon
      font-size: 30px
</style>
