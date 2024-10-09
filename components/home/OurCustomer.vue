<template>
  <div class="container" id="customer">
    <Separator>
      <h1
        class="sm:text-xl md:text-5xl font-extrabold text-white whitespace-nowrap"
      >
        A Selection Of Our Customers
      </h1>
    </Separator>

    <Vue3Marquee
      class="relative overflow-hidden my-10 py-6 sm:py-8 lg:py-10"
      :duration="duration"
      :direction="direction"
      :pauseOnHover="true"
    >
      <div
        v-for="(company, index) in companies"
        :key="index"
        class="flex items-center"
      >
        <h2
          class="text-2xl sm:text-3xl lg:text-4xl font-normal mr-20 sm:mr-30 lg:mr-40 whitespace-nowrap"
        >
          {{ company.name }}
        </h2>
      </div>
    </Vue3Marquee>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from "vue";
import { Vue3Marquee } from "vue3-marquee";
import { Separator } from "@/components/ui/separator";
const companies = ref([
  { name: "Get Accept" },
  { name: "Collector Bank" },
  { name: "Bang & Olufsen" },
  { name: "Concito" },
]);

const direction = ref("reverse");
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
