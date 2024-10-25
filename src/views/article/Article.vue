<template>
  <ion-page>
    <ion-content>
      <div class="article-banner">
        <ion-img src="assets/asthma.jpg" class="article-banner-image"></ion-img>
        <div class="article-banner-text">
          <ion-text color="light"
            ><h1>What to do against asthma?</h1>
            <p class="category">
              <ion-badge>Asthma</ion-badge><span> • 2 hours ago</span>
            </p></ion-text
          >
        </div>
      </div>
      <div class="ion-padding">
        <ion-text>
          <h1>World Health Organization</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem
            ipsam autem quibusdam suscipit, nisi beatae impedit, doloribus,
            dolore illum similique quia officia aliquam repudiandae temporibus
            nihil sunt pariatur sint distinctio.
          </p>
          <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam
            sequi ipsum a. Sit ab distinctio obcaecati deleniti, quisquam
            aspernatur delectus quibusdam voluptatibus pariatur, repellendus
            quam similique dolores facere exercitationem impedit mollitia eaque.
            Voluptates vel eum libero ad repudiandae officiis facere error
            molestiae! Fugiat adipisci amet corrupti provident quas voluptate
            repudiandae!
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Labore,
            iusto.
          </p>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquid
            accusantium cupiditate praesentium quia, hic ducimus eaque, itaque
            esse aperiam iste corrupti natus labore excepturi aut fugit veniam.
            Molestias, eos. At tenetur vel quo sed assumenda quis quisquam
            totam. Odit doloremque, pariatur repellat ducimus aliquam magnam
            perspiciatis, voluptatibus culpa iste consectetur officia, adipisci
            dolorum autem veritatis totam vero dignissimos amet sint aut
            voluptatum? Eos tenetur eius sequi qui assumenda optio modi.
          </p>
        </ion-text>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonContent, IonImg, IonText, IonBadge } from "@ionic/vue";
</script>

<style scoped>
.article-banner {
  position: relative;
  height: 400px;
  overflow: hidden;
}
.article-banner-image {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
}

.article-banner-text {
  position: absolute;
  width: 100%;
  left: 0;
  bottom: 0;
  padding: 1rem;
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), #000000);
}

p {
  line-height: 1.7rem;
}

ion-badge {
  --background: white;
  --color: rgb(101, 101, 101);
  --padding-end: 12px;
  --padding-start: 12px;
  --padding-top: 6px;
  --padding-bottom: 6px;
}

.category {
  display: flex;
  gap: 0.5rem;
}
</style>
