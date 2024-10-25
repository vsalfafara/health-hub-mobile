<template>
  <ion-page>
    <ion-content class="ion-padding login" :fullscreen="true">
      <div class="container">
        <ion-text>
          <h1>Welcome to Health Hub</h1>
          <p>
            Don't have an account? <u><b>Create an account</b></u>
          </p>
        </ion-text>
        <form>
          <div class="input">
            <p><b>Email</b></p>
            <ion-input
              type="email"
              fill="outline"
              placeholder="john@example.com"
            ></ion-input>
          </div>
          <div class="input">
            <p><b>Password</b></p>
            <ion-input type="password" fill="outline">
              <ion-input-password-toggle
                slot="end"
                color="dark"
              ></ion-input-password-toggle>
            </ion-input>
          </div>
          <ion-button
            expand="block"
            class="sign-in ion-margin-bottom"
            href="/tabs/dashboard"
          >
            Sign In
          </ion-button>
          <p class="or">Or sign in via</p>
          <ion-button expand="block" class="custom ion-margin-bottom">
            <ion-icon slot="start" src="assets/icons/google/48.svg"></ion-icon>
            Sign In with Google</ion-button
          >
          <ion-button expand="block" class="custom ion-margin-bottom">
            <ion-icon
              slot="start"
              src="assets/icons/microsoft/48.svg"
            ></ion-icon>
            Sign In with Microsoft</ion-button
          >
          <ion-button expand="block" class="custom ion-margin-bottom">
            <ion-icon slot="start" src="assets/icons/sso/50.svg"></ion-icon>
            Sign In with SSO</ion-button
          >
        </form>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import {
  IonPage,
  IonContent,
  IonText,
  IonInput,
  IonButton,
  IonIcon,
  IonInputPasswordToggle,
} from "@ionic/vue";
</script>

<style scoped>
.container {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
}

form {
  margin: 1rem 0;
  width: 100%;
}

.container .input {
  width: 100%;
  margin-bottom: 2rem;
}

.or {
  text-align: center;
}

.sign-in {
  --background: #2f2f2f;
  --background-hover: #4f4f4f;
  --background-activated: #4f4f4f;
  --background-focused: #4f4f4f;

  --color: rgb(255, 255, 255);

  --border-radius: 0;

  --box-shadow: 0 2px 6px 0 rgb(0, 0, 0, 0.25);

  --ripple-color: rgb(157, 157, 157);

  --padding-top: 10px;
  --padding-bottom: 10px;
}

.custom {
  --background: #f3f3f3;
  --background-hover: #d5d5d5;
  --background-activated: #d5d5d5;
  --background-focused: #d5d5d5;

  --color: #2f2f2f;

  --border-radius: 0;

  --box-shadow: 0 2px 6px 0 rgb(0, 0, 0, 0.25);

  --ripple-color: rgb(118, 118, 118);

  --padding-top: 10px;
  --padding-bottom: 10px;
}
</style>
