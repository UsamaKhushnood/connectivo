<template>
  <div
    class="min-h-screen flex flex-col items-center justify-center text-white p-8 bg-gradient-to-br from-blue-950 via-black to-blue-400 -mt-[55px]"
  >
    <h1 class="text-4xl md:text-8xl mt-20 md:mt-0 font-bold mb-4 text-center capitalize">
      Connect the <span class="text-primary">dots</span>
    </h1>
    <p class="text-xl mb-8 text-center max-w-2xl">
      Free up your time by connecting the systems you depend on, by a provider
      you can count on.
    </p>
    <div class="flex md:flex-row flex-col md:space-x-4 mb-12">
      <router-link to="/products">
        <Button class="rounded-full">View SaaS Products</Button>
      </router-link>
      <router-link :to="{ path: '/', hash: '#services' }">
        <Button
          class="rounded-full gap-2 bg-transparent hover:bg-transparent hover:underline border-0"
          variant="outline"
        >
          View Custom Software Services <ChevronRight size="16" />
        </Button>
      </router-link>
    </div>
    <div
      class="bg-black border bg-opacity-30 p-6 rounded-3xl flex flex-col items-center text-center mb-12 max-w-3xl"
    >
      <h3 class="text-lg md:text-3xl font-semibold mb-2 capitalize">
        Your technology partner for digital solutions.
      </h3>
      <p class="text-sm md:text-base">
        Connectivo assists SME companies in optimizing, connecting, and
        improving their business processes. We are small enough to see, listen,
        and care about our customers' success, yet big enough to engage, push,
        and deliver software that allows businesses to reach their target goals.
      </p>
    </div>
    <div class="flex flex-wrap justify-center items-center gap-8">
      <img
        v-for="(platform, index) in reviewPlatforms"
        :key="index"
        :src="platform.image"
        :alt="platform.name"
        class="h-12 rounded-full cursor-pointer"
      />
    </div>
  </div>
</template>

<script setup>
import { ChevronRight } from "lucide-vue-next";
const reviewPlatforms = [
  { image: "/customers/bo.jpeg" },
  { image: "/customers/cb.png" },
  { image: "/customers/concito.png" },
  { image: "/customers/ga.png" },
];
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
</style>
