<template>
  <section id="process" class="text-white p-8 md:py-[150px]">
    <div class="max-w-7xl mx-auto ">
      <h1
        class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold mb-10 sm:mb-16 md:mb-20 text-center"
      >
        Our
        <span class="text-primary">Process</span>
      </h1>
      <div class="relative ">
        <div
          class="absolute left-0 sm:left-1/2 top-0 bottom-0 transform sm:-translate-x-1/2 w-0.5 bg-primary"
        ></div>
        <div class="space-y-8 sm:space-y-16">
          <div
            v-for="(step, index) in processSteps"
            :key="index"
            class="relative flex flex-col sm:flex-row items-start sm:items-center mb-8 sm:mb-0"
          >
            <div
              class="absolute left-0 sm:left-1/2 transform -translate-x-1/2 mt-6 sm:mt-0"
            >
              <div
                class="w-12 h-12 bg-gradient-to-b from-[#15231C] via-[#101010] to-[#1F2418] border border-primary rounded-full flex items-center justify-center"
              >
                <component :is="step.icon" class="w-6 h-6 text-primary" />
              </div>
            </div>
            <div
              :class="[
                'w-full sm:w-1/2 md:pl-16 pl-10 sm:pl-0 sm:pr-8 md:pr-16',
                index % 2 === 0
                  ? 'sm:ml-auto sm:text-left'
                  : 'sm:text-right md:text-start',
              ]"
            >
              <h3 class="text-3xl font-bold mb-2">{{ step.title }}</h3>
              <p class="text-gray-400">{{ step.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { ChartNoAxesColumn, CodeIcon, Truck } from "lucide-vue-next";

const processSteps = ref([
  {
    title: "Situation and strategy analysis",
    description:
      "There's a lot that we do before actually starting the project. Market research and analysis, studying and understanding the technical documentation to assess the limitations and possibilities between apps, listening to the clients' needs and preferences, consulting with stakeholders and finally coming up with a high-level mapping. With emphasis on planning and problem solving, the client can expect to receive a clear execution plan.",
    icon: ChartNoAxesColumn,
  },
  {
    title: "Development Plan & Production",
    description:
      "With an accepted offer and agreed upon strategy, the craftsmanship starts to convert ideas, needs and demands from concept to code. Each project is led by at least one project manager and depending on the client's budget, one or several seasoned developers. Our experience in custom application development has contributed to the formation and growth of companies in a variety of industries. Every developer in our team understands that clients depend on the quality of their work, thus, put all efforts to give the best result possible.",
    icon: CodeIcon,
  },
  {
    title: "Delivery & Follow-up",
    description:
      "After close contact and careful development, delivery of the product / service follows. A quality review is done to see that everything is up to standard. Should any errors or bumps still creep in, we have a guarantee that covers errors that are discovered within 30 days of delivery free of charge to ensure the client's needs are met.",
    icon: Truck,
  },
]);
</script>

<style scoped>
@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (min-width: 640px) {
  .relative:nth-child(odd) {
    animation: fadeInLeft 0.6s ease-out forwards;
  }

  .relative:nth-child(even) {
    animation: fadeInRight 0.6s ease-out forwards;
  }
}

.relative:nth-child(1) {
  animation-delay: 0.1s;
}
.relative:nth-child(2) {
  animation-delay: 0.3s;
}
.relative:nth-child(3) {
  animation-delay: 0.5s;
}
</style>
