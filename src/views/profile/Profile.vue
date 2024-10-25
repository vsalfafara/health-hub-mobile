<template>
  <ion-page>
    <Navigation />
    <ion-content class="ion-padding">
      <h1 class="ion-text-center">John Doe</h1>
      <ion-avatar>
        <ion-img src="assets/profile.jpg"></ion-img>
      </ion-avatar>
      <ion-grid>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Date of Birth:</b></ion-col>
          <ion-col>01.01.1980</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Gender:</b></ion-col>
          <ion-col>Male</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Email:</b></ion-col>
          <ion-col>john.doe@example.com</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Phone:</b></ion-col>
          <ion-col>+1 212 555 1212</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Blood Type:</b></ion-col>
          <ion-col>B-</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>SSN:</b></ion-col>
          <ion-col>123-45-6789</ion-col>
        </ion-row>
        <ion-row class="ion-margin-bottom">
          <ion-col size="4"><b>Allergies:</b></ion-col>
          <ion-col>Penicillin, Peanuts, Dust Mites, Shellfish </ion-col>
        </ion-row>
      </ion-grid>
      <div class="profile-action">
        <ion-button color="danger" href="/">Logout</ion-button>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import Navigation from "@/components/Navigation.vue";
import {
  IonPage,
  IonContent,
  IonAvatar,
  IonGrid,
  IonRow,
  IonCol,
  IonImg,
  IonButton,
} from "@ionic/vue";
</script>

<style scoped>
ion-avatar {
  height: 100px;
  width: 100px;
  display: block;
  margin: 0 auto 2rem;
}
.profile-action {
  display: flex;
  justify-content: flex-end;
}
</style>
