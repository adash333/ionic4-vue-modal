<template>
  <div>
    <ion-header>
      <ion-toolbar color="success">
        <ion-title>{{ title }}</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content padding>
      <p>{{ content }}</p>
      <p>random number: {{ userData }}</p>
      <div text-center>
        <ion-button @click="closeModal">close modal</ion-button>
      </div>
    </ion-content>
  </div>
</template>

<script>
export default {
  name: "Modal",
  props: {
    title: { type: String, default: "Super Modal" },
    userData: { type: Number, default: 1 }
  },
  data() {
    return {
      content: "Content"
    };
  },
  methods: {
    closeModal() {
      return this.$ionic.modalController.dismiss();
    }
  }
};
</script>
