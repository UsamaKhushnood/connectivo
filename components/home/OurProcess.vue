<template>
  <section id="process" class="relative overflow-hidden bg-[url('/block.png')]">
    <div
      class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]"
    ></div>
    <div class="absolute inset-0 -skew-y-6 origin-right">
      <div class="bg-primary w-[500px] h-12 absolute left-0 -top-[50px]">
        <div
          class="bg-[#2176e4b4] w-[250px] h-12 absolute left-[180px] -top-[30px]"
        ></div>
      </div>
    </div>

    <div class=" container relative z-10 md:py-[300px] pt-[100px] pb-[250px]">
      <h1
        class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold mb-10 sm:mb-16 md:mb-20 md:text-center"
      >
        Our <span class="text-primary">Process</span>
      </h1>
      <div>
        <!-- Step 1 -->
        <div class="relative flex md:flex-col gap-6 items-center md:pb-10 pb-6">
          <div
            class="bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 md:w-20 md:h-20 flex items-center justify-center md:mb-4"
          >
            <ChartNoAxesColumn class="text-primary" size="30" />
          </div>
          <span class="md:text-2xl font-medium md:mb-10">
            Situation and Strategy Analysis
          </span>
          <img
            src="/arrow.svg"
            class="absolute bottom-7 translate-y-1/2 -rotate-90 w-16 h-auto hidden md:block"
          />
        </div>

        <div
          class="bg-gradient-to-br from-[#69ff64] via-[#111] to-[#69ff64] h-0.5 hidden md:block"
        ></div>

        <div class="md:flex justify-between md:pl-10 md:pr-20">
          <!-- Step 2 -->
          <div
            class="relative flex md:flex-col gap-6 items-center pb-6"
            @mouseenter="
              hoveredPlatform = {
                name: 'Development Plan & Production',
                description:
                  'We convert ideas into code, working with developers and project managers for smooth execution.',
              }
            "
            @mouseleave="hoveredPlatform = null"
          >
            <div
              class="md:mt-20 bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 md:w-20 md:h-20 flex items-center justify-center md:mb-4"
            >
              <CodeIcon class="text-primary" size="30" />
            </div>
            <span class="md:text-2xl font-medium">
              Development Plan & Production
            </span>
            <img
              src="/arrow.svg"
              class="absolute transform -translate-y-1/2 top-8 rotate-90 w-16 hidden md:block"
            />
          </div>

          <!-- Step 3 -->
          <div
            class="relative flex md:flex-col gap-6 items-center"
            @mouseenter="
              hoveredPlatform = {
                name: 'Delivery & Follow-up',
                description:
                  'After delivery, we perform quality reviews and offer a 30-day guarantee for adjustments.',
              }
            "
            @mouseleave="hoveredPlatform = null"
          >
            <div
              class="md:mt-20 bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 md:w-20 md:h-20 flex items-center justify-center mb-4"
            >
              <Truck class="text-primary" size="30" />
            </div>
            <span class="md:text-2xl font-medium"> Delivery & Follow-up </span>
            <img
              src="/arrow.svg"
              class="absolute transform -translate-y-1/2 top-8 rotate-90 w-16 hidden md:block"
            />
          </div>
        </div>

        <!-- <Transition name="fade">
          <div
            v-if="hoveredPlatform"
            class="fixed bottom-12 right-8 bg-gradient-to-b from-[#101010] via-[#101010] to-[#000000] rounded-2xl border z-10 p-6 md:max-w-2xl"
          >
            <h2 class="text-2xl font-bold mb-2">{{ hoveredPlatform.name }}</h2>
            <p class="text-gray-400">{{ hoveredPlatform.description }}</p>
          </div>
        </Transition> -->
      </div>
    </div>
    <div class="bg-primary w-[500px] h-12 absolute -skew-y-6 right-0 bottom-20">
      <div
        class="bg-[#2176e4b4] w-[250px] h-12 absolute left-[180px] -top-6"
      ></div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { ChartNoAxesColumn, CodeIcon, Truck } from "lucide-vue-next";

const hoveredPlatform = ref(null);
</script>
