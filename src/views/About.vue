<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Hello World</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <div text-center>
        <h1>This is an about page</h1>
      </div>
      <router-link to="/">
        <ion-button color="secondary" expand="full">Home</ion-button>
      </router-link>

      <div text-center>
        <ion-button color="success" fill="outline" @click="openModal">Open Modal</ion-button>
      </div>
      <ion-card>
        <img alt="madison.jpg" src="../assets/madison.jpg">
        <ion-card-header>
          <ion-card-subtitle>Card Subtitle</ion-card-subtitle>
          <ion-card-title>Card Title</ion-card-title>
        </ion-card-header>

        <ion-card-content>
          Keep close to Nature's heart... and break clear away, once in awhile,
          and climb a mountain or spend a week in the woods. Wash your spirit clean.
        </ion-card-content>
      </ion-card>

      <ion-card>
        <ion-item href="#">
          <ion-icon name="wifi" slot="start"></ion-icon>
          <ion-label>Card Link Item 1</ion-label>
        </ion-item>

        <ion-item href="#">
          <ion-icon name="wine" slot="start"></ion-icon>
          <ion-label>Card Link Item 2</ion-label>
        </ion-item>

        <ion-item>
          <ion-icon name="warning" slot="start"></ion-icon>
          <ion-label>Card Button Item 1</ion-label>
        </ion-item>

        <ion-item>
          <ion-icon name="walk" slot="start"></ion-icon>
          <ion-label>Card Button Item 2</ion-label>
        </ion-item>
      </ion-card>
    </ion-content>
  </div>
</template>

<script>
import Modal from "./Modal.vue";

export default {
  name: "about",
  methods: {
    openModal() {
      return this.$ionic.modalController
        .create({
          component: Modal,
          componentProps: {
            data: {
              content: "New Content"
            },
            propsData: {
              title: "New title",
              userData: Math.round(Math.random() * 100)
            }
          }
        })
        .then(m => m.present());
    }
  }
};
</script>