<template>
  <swiper
    :modules="[Navigation]"
    :slides-per-view="1"
    :centered-slides="true"
    :space-between="spaceBetween"
    :navigation="true"
    :loop="false"
    class="mySwiper"
    :initial-slide="initialSlide"
  >
    <swiper-slide
      v-for="(person, index) in people"
      :key="index"
      class="swiper-slide-custom"
    >
      <div class="card">
        <q-img :src="person.image" alt="Profile Image" class="profile-image" />
        <h2>{{ person.name }}</h2>
        <p>{{ person.position }} · {{ person.experience }}</p>
        <div class="skills">
          <q-chip
            v-for="(skill, index) in person.skills"
            :key="index"
            outline
            class="skill"
          >
            {{ skill }}
          </q-chip>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script setup>
import { ref, computed } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";
import { Navigation } from "swiper/modules";

const people = [
  {
    name: "Abhishek Gupta",
    position: "마케팅",
    experience: "2y+",
    image: "../src/static/profiles/profphoto.jpg",
    skills: [
      "마케팅 콘텐츠 제작",
      "인스타그램 관리",
      "트위터 관리",
      "블로그 글 작성",
    ],
  },
  {
    name: "Robert Kanyoro",
    position: "마케팅",
    experience: "2y+",
    image: "../src/static/profiles/profphoto.jpg",
    skills: [
      "마케팅 콘텐츠 제작",
      "인스타그램 관리",
      "트위터 관리",
      "블로그 글 작성",
    ],
  },
  {
    name: "Esther Wahu",
    position: "마케팅",
    experience: "2y+",
    image: "../src/static/profiles/profphoto.jpg",
    skills: [
      "마케팅 콘텐츠 제작",
      "인스타그램 관리",
      "트위터 관리",
      "블로그 글 작성",
    ],
  },
];

const breakpoints = {
  240: {
    slidesPerView: 1,
  },
  768: {
    slidesPerView: 3,
  },
  1024: {
    slidesPerView: 3,
  },
};

const initialSlide = ref(1);

const spaceBetween = computed(() => {
  return window.innerWidth <= 768 ? -100 : -600;
});
</script>

<style scoped>
.mySwiper {
  width: 100%;
  padding: 40px 0;
}

.card {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 300px;
  transition: transform 0.3s, height 0.3s, opacity 0.3s;
}

.profile-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 20px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.skill {
  margin: 5px;
}

.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s, opacity 0.3s;
  z-index: 1;
  opacity: 0.3;
  transform: scale(0.8);
}

.swiper-button-prev,
.swiper-button-next {
  color: #fff;
  background-color: rgba(0, 0, 0, 0.5); /* Background color */
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.swiper-button-prev:hover,
.swiper-button-next:hover {
  background-color: rgba(0, 0, 0, 0.7); /* Hover background color */
}

.swiper-slide-active {
  opacity: 1;
  transform: scale(1);
  z-index: 2;
}
</style>
