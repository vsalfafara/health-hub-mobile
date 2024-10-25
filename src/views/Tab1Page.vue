<template>
  <ion-page>
    <Navigation />
    <ion-content class="ion-padding">
      <ion-text>
        <h1>Newest Articles</h1>
      </ion-text>
      <swiper
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide
          class="carousel-slide"
          @click="navigate('/tabs/article1')"
        >
          <ion-img src="assets/asthma.jpg" class="article"> </ion-img>
          <ion-badge>Asthma</ion-badge>
          <div class="slide-text">
            <ion-text color="light"
              ><h1>What to do against asthma?</h1>
              <p>Trending • 2 hours ago</p></ion-text
            >
          </div>
        </swiper-slide>
        <swiper-slide class="carousel-slide"
          ><ion-img src="assets/heartattack.jpg" class="article"> </ion-img>
          <ion-badge class="alert">Alert</ion-badge>
          <div class="slide-text">
            <ion-text color="light"
              ><h1>Heart attack cases rising</h1>
              <p>Trending • 3 hours ago</p>
            </ion-text>
          </div>
        </swiper-slide>
      </swiper>
      <ion-text>
        <h1>Recommended</h1>
      </ion-text>
      <div class="recommendation">
        <ion-img src="assets/asthma.jpg" class="recommendation-image">
        </ion-img>
        <div class="recommendation-text">
          <ion-text>
            <p class="category">Asthma</p>
            <h3>What to do against asthma?</h3>
            <ion-avatar class="recommendation-avatar">
              <img
                src="https://ionicframework.com/docs/img/demos/avatar.svg"
                alt=""
              />
            </ion-avatar>
          </ion-text>
        </div>
      </div>
      <div class="recommendation">
        <ion-img src="assets/heartattack.jpg" class="recommendation-image">
        </ion-img>
        <div class="recommendation-text">
          <ion-text>
            <p class="category">Alert</p>
            <h3>Heart attack cases rising</h3>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam
              facere, fugit est ullam tempore nisi recusandae dolorem blanditiis
              libero molestias.
            </p>
          </ion-text>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import {
  IonPage,
  IonContent,
  IonText,
  IonImg,
  IonBadge,
  IonAvatar,
} from "@ionic/vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import Navigation from "@/components/Navigation.vue";
import { useRouter } from "vue-router";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

const router = useRouter();

const onSwiper = (swiper: any) => {
  console.log(swiper);
};
const onSlideChange = () => {
  console.log("slide change");
};

const navigate = (link: string) => {
  router.push(link);
};
</script>

<style>
.carousel-slide {
  height: 300px !important;
  position: relative;
  padding: 2rem;
}
.article {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
}

.slide-text {
  position: absolute;
  width: 100%;
  left: 0;
  bottom: 0;
  padding: 1rem;
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), #000000);
}

.recommendation {
  display: grid;
  grid-template-columns: 150px auto;
  margin-bottom: 1rem;
}

.recommendation-image {
  height: 150px;
  width: 150px;
  object-fit: cover;
}

.recommendation-text {
  margin-left: 1rem;
}
ion-badge {
  --background: white;
  --color: rgb(101, 101, 101);
  --padding-end: 12px;
  --padding-start: 12px;
  --padding-top: 6px;
  --padding-bottom: 6px;
}

ion-badge.alert {
  --background: red;
  --color: white;
}

.category {
  font-size: 0.8rem;
  color: rgb(124, 124, 124);
  margin-bottom: 0.5rem;
}

h3 {
  margin-top: 0;
}

.recommendation-text ion-text {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.recommendation-avatar {
  height: 2rem;
  width: 2rem;
  margin-top: auto;
}
</style>
