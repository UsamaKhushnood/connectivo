<template>
  <div class="bg-secondary">
    <div class="3xl:container" id="customer">
      <Vue3Marquee
        class="relative overflow-hidden py-6 sm:py-8 lg:py-6"
        clone
        :duration="duration"
      >
        <div
          v-for="(company, index) in companies"
          :key="index"
          class="flex items-center"
        >
          <h2
            class="text-xl sm:text-3xl lg:text-3xl font-normal mr-20 sm:mr-30 lg:mr-20 whitespace-nowrap"
          >
            {{ company.name }}
          </h2>
        </div>
      </Vue3Marquee>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from "vue";
import { Vue3Marquee } from "vue3-marquee";

const companies = ref([
  { name: "Get Accept" },
  { name: "Collector Bank" },
  { name: "Bang & Olufsen" },
  { name: "Concito" },
]);

const baseSpeed = 50; // pixels per second
const speedMultiplier = ref(1);

const duration = computed(() => {
  const totalWidth = companies.value.length * 300; // Approximate width of each company name
  return totalWidth / (baseSpeed * speedMultiplier.value);
});

const updateSpeedMultiplier = () => {
  if (window.innerWidth < 640) {
    speedMultiplier.value = 0.7;
  } else if (window.innerWidth < 1024) {
    speedMultiplier.value = 0.85;
  } else {
    speedMultiplier.value = 1;
  }
};

onMounted(() => {
  updateSpeedMultiplier();
  window.addEventListener("resize", updateSpeedMultiplier);
});

onUnmounted(() => {
  window.removeEventListener("resize", updateSpeedMultiplier);
});
</script>
<style>
.separator-label {
  font-size: 200px !important;
}
</style>
