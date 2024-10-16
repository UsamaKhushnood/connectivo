<template>
  <div
    class="bg-[#191d23] py-8 md:pt-8 px-8 md:pb-5 rounded-2xl feature-card relative"
  >
    <div class="card-gradient-border">
      <div class="flex justify-center items-center">
        <div class="relative">
          <EllipseIcon class="w-12 h-12 text-gray-700" />
          <div
            class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2"
          >
            <slot name="icon"></slot>
          </div>
        </div>
      </div>
      <h4 class="mb-2 mt-6 text-xl font-bold text-white">{{ title }}</h4>
      <p class="text-gray-300 text-sm">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import EllipseIcon from "@/components/icons/EllipseIcon.vue";
const props = defineProps({
  title: String,
  description: String,
});
</script>

<style scoped>
.card-gradient-border::before,
.card-gradient-border::after {
  content: "";
  background: linear-gradient(
    rgba(255, 255, 255, 0),
    rgba(255, 255, 255, 0.42),
    rgba(255, 255, 255, 0)
  );
  position: absolute;
  height: 50%;
  width: 2px;
  border-radius: 50px;
  top: 50%;
  transform: translate(-50%, -50%);
}
.card-gradient-border::before {
  left: 0;
}
.card-gradient-border::after {
  right: 0;
}
</style>
