<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Hello World</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <div text-center>
        <h1>Welcome To @ionic/vue</h1>
        <img alt="Vue logo" src="../assets/logo.png">
      </div>
      <router-link to="/about">
        <ion-button color="primary" expand="full">About</ion-button>
      </router-link>
    </ion-content>
  </div>
</template>

<script>
export default {
  name: "home"
};
</script>