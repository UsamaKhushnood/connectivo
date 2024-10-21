<script setup lang="ts">
import TheFooter from "~/components/common/TheFooter.vue";
import TheHeader from "~/components/common/TheHeader.vue";
import ContactUs from "~/components/home/ContactUs.vue";
import ContactUs1 from "~/components/home/ContactUs1.vue";
</script>

<template>
  <div class="default">
    <TheHeader />
    <div class="min-h-dvh"><slot></slot></div>
    <ContactUs />
    <ContactUs1 />
    <TheFooter />
  </div>
</template>
