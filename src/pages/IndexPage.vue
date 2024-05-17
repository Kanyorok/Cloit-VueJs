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
/* Default styles */
.border-top-white {
  border-top: 2px solid #fff;
  border-width: 3px;
  margin-right: 15px;
}
.border-top-white p {
  font-family: Roboto;
  font-weight: 400;
  font-size: 16px;
}
.aligned-left {
  text-align: left;
}
.main-section {
  padding-top: 40px;
  text-align: left;
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
  padding: 0px 100px;
}

/* Styles for mobile devices */
@media (max-width: 767px) {
  .main-section {
    padding-top: 20px;
    text-align: left;
    color: #fff;
  }
  .header-view {
    display: flex;
    flex-direction: column;
  }
  .swiper-button-next {
    color: #fff !important;
  }
  .q-btn-group {
    display: none;
  }
  .main-section h1 {
    font-size: 32px;
    line-height: 42px;
  }
  .main-section-paragraph {
    font-size: 18px;
    line-height: 28px;
  }
  .header-view {
    padding: 0px 20px;
  }
  .border-top-white {
    margin-right: 10px;
  }
  .border-top-white p {
    font-size: 14px;
  }
}

/* Styles for tablets and larger screens */
@media (min-width: 768px) {
  .main-section {
    padding-top: 40px;
    text-align: left;
    color: #fff;
  }
  .main-section h1 {
    font-size: 48px;
    line-height: 62.4px;
  }
  .main-section-paragraph {
    font-size: 24px;
    line-height: 34px;
  }
  .header-view {
    padding: 0px 100px;
  }
  .border-top-white {
    margin-right: 15px;
  }
  .border-top-white p {
    font-size: 16px;
  }
}

/* Styles for larger desktop screens */
@media (min-width: 1024px) {
  .main-section {
    padding-top: 60px;
    text-align: left;
    color: #fff;
  }
  .main-section h1 {
    font-size: 56px;
    line-height: 70px;
  }
  .main-section-paragraph {
    font-size: 28px;
    line-height: 38px;
  }
  .header-view {
    padding: 0px 120px;
  }
  .border-top-white {
    margin-right: 20px;
  }
  .border-top-white p {
    font-size: 18px;
  }
}
</style>

<script setup>
import SliderLink from "components/SliderLink.vue";
defineOptions({
  name: "IndexPage",
});
</script>
