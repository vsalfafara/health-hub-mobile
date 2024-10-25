<template>
  <ion-header class="ion-no-border">
    <ion-toolbar>
      <ion-buttons slot="start">
        <ion-menu-button></ion-menu-button>
      </ion-buttons>
      <ion-buttons slot="end">
        <ion-button>
          <ion-icon slot="icon-only" :icon="search"></ion-icon>
        </ion-button>
        <ion-avatar>
          <ion-img src="assets/profile.jpg" />
        </ion-avatar>
      </ion-buttons>
    </ion-toolbar>
  </ion-header>
</template>

<script setup lang="ts">
import {
  IonHeader,
  IonToolbar,
  IonButtons,
  IonMenuButton,
  IonIcon,
  IonButton,
  IonAvatar,
  IonImg,
} from "@ionic/vue";
import { search, notifications } from "ionicons/icons";
</script>

<style scoped>
ion-avatar {
  width: 40px;
  height: 40px;
}
</style>
