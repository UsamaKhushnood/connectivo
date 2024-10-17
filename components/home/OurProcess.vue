<template>
  <div id="process" class="container py-[150px]">
    <h1
      class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold mb-10 sm:mb-16 md:mb-20"
    >
      Our
      <span class="text-primary">Process </span>
    </h1>
    <div class="relative">
      <!-- Icons aligned horizontally -->
      <div class="flex justify-between items-center relative">
        <div
          v-for="(platform, index) in platforms"
          :key="platform.name"
          class="flex flex-col items-center"
          :class="index === 1 ? 'md:mb-[165px] mb-[180px]' : 'md:mt-[163px] mt-[180px]'"
        >
          <!-- Blue Line Above (For Even Indexes) -->
          <div
            v-if="index % 2 === 0"
            class="h-8 w-0.5 bg-primary"
            aria-hidden="true"
          ></div>

          <!-- Platform Icon -->

          <div
            class="bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 w-20 h-20 flex items-center justify-center mb-4"
            @mouseenter="hoveredPlatform = platform"
            @mouseleave="hoveredPlatform = null"
          >
            <component :is="platform.icon" class="text-primary" size="30" />
          </div>
          <span class="md:text-2xl font-medium">
            {{ platform.name }}
          </span>

          <!-- Red Line Below (For Odd Indexes) -->
          <div
            v-if="index % 2 !== 0"
            class="mt-2 h-8 w-0.5 bg-primary"
            aria-hidden="true"
          ></div>
        </div>
      </div>

      <!-- Horizontal Line -->
      <div
        class="absolute left-0 right-0 top-1/2 border-t-2 border-primary"
        aria-hidden="true"
      ></div>
    </div>

    <!-- Tooltip Section -->
    <Transition name="fade">
      <div
        v-if="hoveredPlatform"
        class="fixed bottom-8 right-8 bg-gradient-to-b from-[#101010] via-[#101010] to-[#000000] rounded-2xl border z-10 p-6 md:max-w-2xl"
      >
        <h2 class="text-2xl font-bold mb-2">
          {{ hoveredPlatform.name }}
        </h2>
        <p class="text-gray-400">{{ hoveredPlatform.description }}</p>
      </div>
    </Transition>
  </div>
</template>
<script setup>
import { ref } from "vue";
import { ChartNoAxesColumn, CodeIcon, Truck } from "lucide-vue-next"; // Import specific icons

const platforms = [
  {
    name: "Situation and Strategy Analysis",
    icon: ChartNoAxesColumn,
    description:
      "There's a lot that we do before actually starting the project. Market research and analysis, studying and understanding the technichal documentation to asses the limitations and possibilities between apps, listening in on the clients’ needs and preferences, consulting with stakeholders and finally coming up with a high-level mapping. With emphasiz on planning and problem solving the client can expect to receive a clear execution plan..",
  },
  {
    name: "Development Plan & Production",
    icon: CodeIcon,
    description:
      "With an accepted offer and agreed upon strategy, the craftmanship starts to convert ideas, needs and demands from concept to code. Each project is lead by minimum one project manager and depening on the clients budget, one or several seasoned developers. Our experience in custom application development had contributed to the formation and growth of companies in a variety of industries. Every developer in our team understands that clients depend on the quality of their work, thus, put all efforts to give the best result possible.",
  },
  {
    name: "Delivery & Follow-up",
    icon: Truck,
    description:
      "After close contact and careful development, delivery of the product / service follows. A quality review is done to see that everything is up to standard. Should any errors or bumps still creep in, we have a guarantee that covers errors that are discovered within 30 days of delivery free of charge to ensure the clients needs are met .",
  },
];

const hoveredPlatform = ref(null);
</script>
