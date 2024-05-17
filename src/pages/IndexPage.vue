<template>
  <q-page class="bg-secondary">
    <div class="row bg-primary">
      <div class="col">
        <div class="main-section">
          <h1>Looking for foreign talent with top capabilities?</h1>
          <p>
            With Hyperhire, you can quickly find the best foreign talent. Meet
            top-tier talents instantly by clicking below.
          </p>
          <q-btn-group flat>
            <q-btn label="Visa Talent" />
            <q-btn label="Permanent Residence" />
            <q-btn label="F-4 (Overseas Koreans)" />
            <q-btn label="General" />
          </q-btn-group>
        </div>
      </div>
      <div class="col">
        <SliderLink />
      </div>
    </div>
  </q-page>
</template>

<style scoped>
.main-section {
  text-align: Left;
  color: #fff;
}
.main-section h1 {
  font-family: Poppins;
  font-weight: 900;
  font-size: 48px;
  line-height: 62.4px;
}
</style>

<script setup>
import SliderLink from "components/SliderLink.vue";
defineOptions({
  name: "IndexPage",
});
</script>
