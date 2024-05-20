<template>
  <div class="button-container">
    <button class="carousel-btn" @click="alertMessage('해외 마케팅')">
      <q-img
        src="../static/icons/icon1.png"
        style="width: 60px; margin-left: 13px"
      ></q-img>
      <p class="btn-text">해외 마케팅</p>
    </button>
    <button class="carousel-btn" @click="alertMessage('퍼블리셔')">
      <q-img
        src="../static/icons/icon2.png"
        style="width: 60px; margin-left: 13px"
      ></q-img>
      <p class="btn-text">해외 마케팅</p>
    </button>
    <button class="carousel-btn" @click="alertMessage('카드월(제도사)')">
      <q-img
        src="../static/icons/icon3.png"
        style="width: 60px; margin-left: 13px"
      ></q-img>
      <p class="btn-text">해외 마케팅</p>
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    alertMessage(msg) {
      alert(`Clicked: ${msg}`);
    },
  },
};
</script>

<style scoped>
.button-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  padding: 20px 0;
}

.btn-text {
  margin-top: 19px;
  margin-left: 15px;
}

.carousel-btn {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 332px;
  height: 88px;
  font-size: 16px;
  background: rgba(255, 255, 255, 0.5);
  border: none;
  color: #006064;
  cursor: pointer;
  transition: background-color 0.3s ease;
  margin-right: 15px;
  border-radius: 8px;
  outline: none;
  padding-left: 16px;
}

.carousel-btn:hover {
  background-color: #b2ebf2;
}
</style>
