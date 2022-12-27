<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
    class="bg-white text-grey-10"
      bordered>
      <q-toolbar class="constrain">
        <q-btn
          flat
          round
          class="large-screen-only q-mr-sm"
          dense
          to="/camera"
          size="18px"
          icon="eva-camera-outline" />
          <q-separator
            vertical
            class="large-screen-only"
            spaced=""
            inset />
        <q-toolbar-title class="text-grand-hotel text-bold"> QuasaGram </q-toolbar-title>
        <q-btn
          flat
          round
          class="large-screen-only"
          dense
          to="/"
          size="18px"
          icon="eva-home-outline" />
      </q-toolbar>
    </q-header>

    <q-footer
      class="bg-white small-screen-only"
      bordered>
        <q-tabs
          class="text-grey-10"
          active-color="primary"
          indicator-color="transparent">
          <q-route-tab
            name="Home"
            icon="eva-home-outline"
            to="/" />
          <q-route-tab
            name="Camera"
            icon="eva-camera-outline"
            to="/camera"/>
        </q-tabs>
    </q-footer>
    <q-page-container class="bg-grey-2">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: "MainLayout",
  data() {
    return {};
  },
};
</script>

<style lang="sass">
.q-toolbar
  @media (min-width: $breakpoint-sm-min)
    height: 77px
.q-toolbar__title
  @media (max-width: $breakpoint-xs-max)
    text-align: center
  font-size: 30px
.q-footer
  .q-tab__icon
    font-size: 30px

.small-screen-only
    @media (max-width: $breakpoint-xs-max)
      display: block
    @media (min-width: $breakpoint-sm-min)
      display: none

.large-screen-only
    @media (max-width: $breakpoint-xs-max)
      display: none
    @media (min-width: $breakpoint-sm-min)
      display: block
</style>
