<template>
  <section class="relative overflow-hidden my-20">
    <div class="container my-20">
      <h2 class="text-4xl md:text-6xl font-extrabold text-center mb-12">
        Our Process
      </h2>
      <div class="relative">
        <div
          class="hidden md:block absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-primary"
        ></div>
        <div class="space-y-12 md:space-y-0">
          <div
            v-for="(step, index) in processSteps"
            :key="index"
            class="process-step relative md:flex md:items-center"
            :class="{ 'md:flex-row-reverse': index % 2 !== 0 }"
          >
            <div
              class="md:w-1/2 md:pr-8"
              :class="{ 'md:pl-8 md:pr-0': index % 2 !== 0 }"
            >
              <div
                class="rounded-2xl border bg-background p-6 outline outline-2 outline-orange-800 outline-offset-[6px] z-10"
              >
                <div
                  class="w-16 h-16 bg-gradient-to-br from-blue-500 to-purple-600 rounded-full flex items-center justify-center mb-4 mx-auto md:mx-0"
                >
                  <component :is="step.icon" class="w-8 h-8 text-white" />
                </div>
                <h3
                  class="text-2xl font-semibold mb-2 text-center md:text-left"
                >
                  {{ step.title }}
                </h3>
                <p class="text-gray-300">{{ step.description }}</p>
              </div>
            </div>
            <div class="hidden md:block md:w-1/2"></div>
          </div>
        </div>
      </div>
      <div
        class="absolute top-0 left-0 w-1/2 h-full bg-[url('/block.png')] rotate-45 translate-x-1/4 -translate-y-1/4"
      ></div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { Lightbulb, Search, Code } from "lucide-vue-next";

const processSteps = ref([
  {
    title: "Situation and strategy analysis",
    description:
      "Theres a lot that we do before actually starting the project. Market research and analysis, studying and understanding the technichal documentation to asses the limitations and possibilities between apps, listening in on the clients’ needs and preferences, consulting with stakeholders and finally coming up with a high-level mapping. With emphasiz on planning and problem solving the client can expect to receive a clear execution plan.",
    icon: Lightbulb,
  },
  {
    title: "Development Plan & Production",
    description:
      "With an accepted offer and agreed upon strategy, the craftmanship starts to convert ideas, needs and demands from concept to code. Each project is lead by minimum one project manager and depening on the clients budget, one or several seasoned developers. Our experience in custom application development had contributed to the formation and growth of companies in a variety of industries. Every developer in our team understands that clients depend on the quality of their work, thus, put all efforts to give the best result possible.",
    icon: Search,
  },
  {
    title: "Delivery & Follow-up",
    description:
      "After close contact and careful development, delivery of the product / service follows. A quality review is done to see that everything is up to standard. Should any errors or bumps still creep in, we have a guarantee that covers errors that are discovered within 30 days of delivery free of charge to ensure the clients needs are met .",
    icon: Code,
  },
]);
</script>
