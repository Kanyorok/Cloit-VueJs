<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="custom-toolbar">
        <q-img src="../static/logo/hyperhire.png" style="width: 114px"></q-img>
        <div class="gt-sm">
          <q-btn
            flat
            label="Login"
            class="q-mr-sm"
            icon-right="keyboard_arrow_down"
          />
          <q-btn flat label="Register" class="q-mr-sm" />
        </div>
        <div class="gt-sm">
          <q-btn push color="white" text-color="primary" label="Contact Us" />
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
        <q-item-label header>
          <q-img src="../static/logo/secologo.png" style="width: 114px"></q-img>
        </q-item-label>

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

<style scoped>
@media (max-width: 767px) {
  .custom-toolbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
@media (min-width: 768px) {
  .custom-toolbar {
    padding: 0 100px 0 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
@media (min-width: 1024px) {
  .custom-toolbar {
    padding: 0 100px 0 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
.gt-sm,
.lt-md {
  display: flex;
  align-items: center;
}
</style>

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
  {
    title: "Contact Us",
    caption: "Contact Hyperhire",
    icon: "mail",
    link: "#",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
