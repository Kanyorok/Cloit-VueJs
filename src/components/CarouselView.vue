<template>
  <div class="button-container">
    <button class="carousel-btn" @click="alertMessage('해외 마케팅')">
      해외 마케팅
    </button>
    <button class="carousel-btn" @click="alertMessage('퍼블리셔')">
      퍼블리셔
    </button>
    <button class="carousel-btn" @click="alertMessage('카드월(제도사)')">
      카드월(제도사)
    </button>
    <button class="carousel-btn" @click="alertMessage('해외 세일즈')">
      해외 세일즈
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

.carousel-btn {
  display: flex;
  align-items: center;
  justify-content: center;
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
}

.carousel-btn:hover {
  background-color: #b2ebf2;
}
</style>
