<template>
  <q-page class="bg-secondary">
    <div class="row bg-primary header-view">
      <div class="col">
        <div class="main-section">
          <h1>Looking for foreign talent with top capabilities?</h1>
          <p class="main-section-paragraph">
            With Hyperhire, you can quickly find the best foreign talent. Meet
            top-tier talents instantly by clicking below.
          </p>
          <q-btn-group flat>
            <div class="border-top-white">
              <span>Visa Talent</span>
              <p>Wages are calculated based on your country.</p>
            </div>
            <div class="border-top-white">
              <span>Permanent Residence</span>
              <p>Don't worry if you don't fit the job when you hire them.</p>
            </div>
            <div class="border-top-white">
              <span>F-4 (Overseas Koreans)</span>
              <p>
                Even if you need someone urgently, quick hiring is possible.
              </p>
            </div>
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
.border-top-white {
  border-top: 2px solid #fff;
  border-width: 3px;
  margin-right: 15px;
}
.border-top-white p {
  font-family: Robot;
  font-weight: 400;
  font-size: 16px;
}
.aligned-left {
  text-align: left;
}
.main-section {
  padding-top: 40px;
  text-align: Left;
  color: #fff;
}
.main-section h1 {
  font-family: Poppins;
  font-weight: 900;
  font-size: 48px;
  line-height: 62.4px;
}
.main-section-paragraph {
  font-family: Poppins;
  font-weight: 900;
  font-size: 24px;
  line-height: 34px;
}
.header-view {
  padding: 0px 100px 0 100px;
}
</style>

<script setup>
import SliderLink from "components/SliderLink.vue";
defineOptions({
  name: "IndexPage",
});
</script>
