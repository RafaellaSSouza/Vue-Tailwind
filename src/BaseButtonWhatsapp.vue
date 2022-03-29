<template>
  <BaseButton :variant="'outline'" type="button" @click="openWhats">
    <IcWhatsApp />
    Conversar no whats
  </BaseButton>
</template>
<script>
  import Vue from "vue";
  import IcWhatsApp from "~/icons/IcWhatsApp.vue";
  import BaseButton from "./BaseButton.vue";

  export default Vue.extend({
    name: "formContact",
    components: { IcWhatsApp, BaseButton },
    methods: {
      openWhats() {
        window.open("https://api.whatsapp.com/send?phone=55159999999999&text=Olá! Gostaria de solicitar um orçamento.");
      },
    },
  });
</script>
