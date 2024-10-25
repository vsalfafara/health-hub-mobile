<template>
  <ion-page>
    <Navigation />
    <ion-content class="ion-padding">
      <ion-text>
        <h1>Hi Von</h1>
        <p>What would you like to do?</p>
      </ion-text>
      <ion-text>
        <h1>Resources</h1>
      </ion-text>
      <div
        class="widget ion-activatable ion-margin-bottom"
        @click="navigate('/tabs/tab1')"
      >
        <ion-text color="light"><h3>Articles</h3></ion-text>
        <ion-ripple-effect></ion-ripple-effect>
        <ion-img src="assets/widgets/article.jpg"></ion-img>
      </div>
      <div class="widget ion-activatable ion-margin-bottom">
        <ion-text color="light"><h3>Videos</h3></ion-text>
        <ion-ripple-effect></ion-ripple-effect>
        <ion-img src="assets/widgets/video.jpg"></ion-img>
      </div>
      <ion-text>
        <h1>Vendors</h1>
      </ion-text>
      <ion-list>
        <ion-item>
          <ion-grid>
            <ion-row>
              <ion-col>
                <div class="app ucm ion-activatable" @click="navigate('/ucm')">
                  <ion-ripple-effect></ion-ripple-effect>
                  <ion-img src="assets/widgets/apps/ucm.png"></ion-img>
                  <ion-text color="light"
                    ><p>
                      Telehealth access to medical care from your phone, tablet,
                      or computer
                    </p></ion-text
                  >
                </div>
              </ion-col>
            </ion-row>
            <ion-row>
              <ion-col>
                <ion-button class="service ucm-service" expand="block">
                  <ion-icon :icon="chatbubbleEllipses" slot="start"></ion-icon>
                  Chat with a Doctor
                </ion-button>
              </ion-col>
              <ion-col>
                <ion-button class="service ucm-service" expand="block">
                  <ion-icon :icon="call" slot="start"></ion-icon>
                  Call a Doctor
                </ion-button>
              </ion-col>
            </ion-row>
          </ion-grid>
        </ion-item>
        <ion-item>
          <ion-grid>
            <ion-row>
              <ion-col>
                <div class="app anura ion-activatable">
                  <ion-ripple-effect></ion-ripple-effect>
                  <ion-img src="assets/widgets/apps/anura.png"></ion-img>
                  <ion-text color="dark"
                    ><p>Take a selfie, know your healthie!</p></ion-text
                  >
                </div>
              </ion-col>
            </ion-row>
            <ion-row>
              <ion-col>
                <ion-button class="service anura-service" expand="block">
                  <ion-icon :icon="camera" slot="start"></ion-icon>
                  Take a selfie
                </ion-button>
              </ion-col>
              <ion-col> </ion-col>
            </ion-row>
          </ion-grid>
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import Navigation from "@/components/Navigation.vue";
import {
  IonPage,
  IonContent,
  IonText,
  IonRippleEffect,
  IonImg,
  IonGrid,
  IonRow,
  IonCol,
  IonButton,
  IonIcon,
  IonList,
  IonItem,
} from "@ionic/vue";
import { call, chatbubbleEllipses, camera } from "ionicons/icons";
import { useRouter } from "vue-router";
const router = useRouter();

function navigate(link: string) {
  router.push(link);
}
</script>

<style scoped>
.widget,
.app {
  position: relative;
  overflow: hidden;
  border: 1px solid #f1f1f1;
  border-radius: 0.3rem;
  gap: 0.5rem;
  padding: 1rem;
}

.widget {
  height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.app {
  min-height: 100px;
}

.widget::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  z-index: 1;
  background-color: rgba(0, 0, 0, 0.4);
}

.widget ion-text {
  z-index: 2;
}

.widget h3 {
  font-size: 2rem;
  margin: 0;
}

.widget ion-img {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -1;
}

.app ion-img {
  height: 60px;
}

.app.ucm {
  background-color: #7c3aed;
}

.app.anura {
  background-color: #4ade80;
}

.app ion-text {
  text-align: center;
}

.service {
  --padding-top: 30px;
  --padding-bottom: 30px;
  --padding-start: 20px;
  --padding-end: 20px;
}

.service.ucm-service {
  --background: #7c3aed;
  --background-hover: rgb(103, 53, 168);
  --background-activated: #5f2eb3;
  --background-focused: #5f2eb3;
  --color: white;
  --ripple-color: #140535;
}

.service.anura-service {
  --background: #4ade80;
  --background-hover: #3fc470;
  --background-activated: #359e5b;
  --background-focused: #272524;
  --color: #272524;
  --ripple-color: #140535;
}
</style>
