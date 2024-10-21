<template>
  <div>
    <HeroSection1 />
    <!-- <ServicesSec2 /> -->
    <ServicesSec />
    <PlatformIntegration />
    <OurProcess />
    <testing />
  </div>
</template>
<script setup>
import HeroSection1 from "~/components/home/HeroSection1.vue";
// import ServicesSec2 from "~/components/home/ServicesSec2.vue";
import ServicesSec from "~/components/home/ServicesSec.vue";
import OurProcess from "~/components/home/OurProcess.vue";
import PlatformIntegration from "~/components/home/PlatformIntegration.vue";
import testing from "~/components/home/testing.vue";
</script>
