<script setup lang="ts">
import TheFooter from "~/components/common/TheFooter.vue";
import TheHeader from "~/components/common/TheHeader.vue";
import ContactUs from "~/components/home/ContactUs.vue";
</script>

<template>
  <div class="default">
    <TheHeader />
    <div class="min-h-dvh"><slot></slot></div>
    <ContactUs />
    <TheFooter />
  </div>
</template>
