<template>
  <div
    class="min-h-screen flex flex-col items-center justify-center text-white p-8"
    :style="backgroundStyle"
  >
    <h1 class="text-5xl font-bold mb-4 text-center" :style="titleStyle">
      Connect the dots.
    </h1>
    <p class="text-xl mb-8 text-center max-w-2xl">
      Free up your time by connecting the systems you depend on, by a provider
      you can count on.
    </p>
    <div class="flex space-x-4 mb-12">
      <router-link to="/products">
        <Button class="rounded-full">View Saas Products </Button>
      </router-link>
      <router-link :to="{ path: '/', hash: '#services' }">
        <Button
          class="rounded-full gap-2 bg-transparent hover:bg-transparent hover:underline border-0 mt-4 md:mt-0"
          variant="outline"
          >View Custom Software Services <ChevronRight size="16"
        /></Button>
      </router-link>
    </div>
    <div
      class="bg-black bg-opacity-30 p-6 rounded-lg flex flex-col items-center text-center"
    >
      <h3 class="text-xl font-semibold mb-2">
        Your technology partner for digital solutions.
      </h3>
      <p>
        Connectivo assists SME companies in optimizing, connecting, and
        improving their business processes. We are small enough to see, listen
        and care about our customers success, yet big enough to engage, push and
        deliver software which allows for businesses to reach their target
        goals.
      </p>
    </div>
    <div class="flex flex-wrap justify-center items-center gap-8">
      <div
        v-for="(name, index) in reviewPlatforms"
        :key="index"
        class="text-gray-400 font-semibold"
      >
        {{ name }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted } from "vue";
import { ChevronRight } from "lucide-vue-next";

const gradientPosition = ref(0);
const reviewPlatforms = ["Capterra", "G2 CROWD", "GetApp", "TrustRadius"];

const backgroundStyle = computed(() => ({
  background: `linear-gradient(135deg, #000 0%, #001a00 ${gradientPosition.value}%, #003300 100%)`,
}));

const titleStyle = computed(() => ({
  textShadow: "0 0 10px rgba(255,255,255,0.5)",
}));

// Animate gradient
onMounted(() => {
  setInterval(() => {
    gradientPosition.value = (gradientPosition.value + 1) % 100;
  }, 50);
});
</script>

<style scoped>
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}

.grid > div {
  animation: float 6s ease-in-out infinite;
}

.grid > div:nth-child(2) {
  animation-delay: -2s;
}

.grid > div:nth-child(3) {
  animation-delay: -4s;
}
</style>
