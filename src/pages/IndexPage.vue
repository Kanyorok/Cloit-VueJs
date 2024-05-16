<template>
  <q-page padding>
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
      <div class="talent-card">
        <q-card>
          <q-card-section>
            <div class="q-gutter-sm">
              <div>Abhishek Gupta</div>
              <div>Nationality: Indian</div>
              <div>Major: Computer Science</div>
              <div>
                Introduction: Graduate from ABC University with 5 years of
                experience in software development.
              </div>
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<style scoped>
.main-section {
  text-align: center;
}
.talent-card {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
</style>

<script setup>
defineOptions({
  name: "IndexPage",
});
</script>
