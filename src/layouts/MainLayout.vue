<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          <q-img
            src="../static/logo/hyperhire.png"
            style="width: 114px"
          ></q-img>
        </q-toolbar-title>
        <div class="gt-sm">
          <q-btn
            flat
            label="Login"
            class="q-mr-sm"
            icon-right="keyboard_arrow_down"
          />
          <q-btn flat label="Register" class="q-mr-sm" />
        </div>
        <div class="lt-md">
          <q-btn
            flat
            dense
            round
            icon="menu"
            aria-label="Menu"
            @click="toggleLeftDrawer"
          />
        </div>
      </q-toolbar>
    </q-header>
    <q-drawer v-model="leftDrawerOpen" bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

defineOptions({
  name: "MainLayout",
});

const linksList = [
  {
    title: "Login",
    caption: "User SignIn",
    icon: "login",
    link: "#",
  },
  {
    title: "Sign Up",
    caption: "Register User",
    icon: "person_add",
    link: "#",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
