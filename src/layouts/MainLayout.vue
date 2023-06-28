<template>
  <q-layout view="hHh lpR lFr">
    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/IndexPage.vue" label="Home" />
        <q-route-tab to="/page2" label="Corsi" />
        <q-route-tab to="/page3" label="About" />
        <q-route-tab to="/page4" label="❁" />
        <q-route-tab to="/page5" label="Log In" />
        <q-route-tab to="/page6" label="Sign In" />
      </q-tabs>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <!-- drawer content -->

      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-icon name="house" />
        </q-item-section>
        <q-item-section> Home </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-icon name="school" />
        </q-item-section>
        <q-item-section> Corsi </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-icon />
        </q-item-section>
        <q-item-section> About </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-icon name="log" />
        </q-item-section>
        <q-item-section> Log In </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section avatar>
          <q-icon name="sign" />
        </q-item-section>
        <q-item-section> Sign In </q-item-section>
      </q-item>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
};
</script>
