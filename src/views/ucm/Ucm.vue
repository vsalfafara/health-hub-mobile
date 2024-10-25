<template>
  <ion-page id="main-content">
    <Navigation />
    <ion-content class="ion-padding">
      <div class="ucm">
        <ion-img src="assets/ucm.svg"></ion-img>
      </div>
      <ion-text>
        <p>
          UCM Digital Telehealth offers you 24/7 access to medical care from
          your phone, tablet, or computer at no additional cost. With our
          virtual healthcare service, you can connect with doctors for
          diagnoses, prescriptions, lab orders, and referrals from the comfort
          of your home. Experience personalized care anytime, anywhere with UCM
          Digital Telehealth, designed to fit your busy lifestyle.
        </p>
      </ion-text>
      <div
        class="options ion-activatable ripple-parent rectangle ion-margin-bottom"
      >
        <ion-ripple-effect></ion-ripple-effect>
        <ion-text color="light" class="schedule">
          <ion-icon :icon="calendar"></ion-icon>
          <h1 class="ion-no-margin">Schedule an Appointment</h1>
        </ion-text>
      </div>
      <div
        class="options ion-activatable ripple-parent rectangle ion-margin-bottom"
      >
        <ion-ripple-effect></ion-ripple-effect>
        <ion-text color="light" class="schedule">
          <ion-icon :icon="videocam"></ion-icon>
          <h1 class="ion-no-margin">Video Call</h1>
        </ion-text>
      </div>
      <div
        class="options ion-activatable ripple-parent rectangle ion-margin-bottom"
      >
        <ion-ripple-effect></ion-ripple-effect>
        <ion-text color="light" class="schedule">
          <ion-icon :icon="call"></ion-icon>
          <h1 class="ion-no-margin">Call a Doctor</h1>
        </ion-text>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import Navigation from "@/components/Navigation.vue";
import {
  IonPage,
  IonContent,
  IonIcon,
  IonImg,
  IonText,
  IonRippleEffect,
} from "@ionic/vue";
import { calendar, videocam, call } from "ionicons/icons";
</script>

<style scoped>
.ucm {
  background-color: #782cd4;
  padding: 2rem;
}

ion-img {
  height: 150px;
}

ion-text {
  line-height: 2rem;
}

ion-icon {
  font-size: 56px;
}

.schedule {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.options {
  height: 100px;
  width: 100%;
  background-color: #250e44;
  padding: 1rem;
  display: flex;
  justify-content: center;
}
.ripple-parent {
  position: relative;
  overflow: hidden;
}
</style>
