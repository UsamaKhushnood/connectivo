<template>
  <section id="process" class="container my-20">
    <h2
      class="text-4xl md:text-6xl font-extrabold text-center mb-12 relative z-10"
    >
      Our Process
    </h2>
    <div>
      <div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
          <div
            v-for="(service, index) in services"
            :key="index"
            :class="[
              'border p-6 bg-background rounded-2xl',
              { 'md:col-span-2': index === 2 },
            ]"
          >
            <div class="flex items-center">
              <component :is="service.icon" class="text-primary mr-2" />
              <h3 class="text-xl font-bold">{{ service.title }}</h3>
            </div>
            <p class="mt-2 pl-8">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { ChartNoAxesColumnIncreasing, Code, Truck } from "lucide-vue-next";

const services = ref([
  {
    title: "Situation and strategy analysis",
    description:
      "There's a lot that we do before actually starting the project. Market research and analysis, studying and understanding the technical documentation to assess the limitations and possibilities between apps, listening in on the clients’ needs and preferences, consulting with stakeholders, and finally coming up with a high-level mapping. With emphasis on planning and problem solving, the client can expect to receive a clear execution plan.",
    icon: ChartNoAxesColumnIncreasing,
  },
  {
    title: "Development Plan & Production",
    description:
      "With an accepted offer and agreed upon strategy, the craftsmanship starts to convert ideas, needs, and demands from concept to code. Each project is led by a minimum of one project manager and, depending on the client's budget, one or several seasoned developers. Our experience in custom application development has contributed to the formation and growth of companies in a variety of industries. Every developer in our team understands that clients depend on the quality of their work and thus put all efforts to give the best result possible.",
    icon: Code,
  },
  {
    title: "Delivery & Follow-up",
    description:
      "After close contact and careful development, delivery of the product/service follows. A quality review is done to see that everything is up to standard. Should any errors or bumps still creep in, we have a guarantee that covers errors discovered within 30 days of delivery free of charge to ensure the client's needs are met.",
    icon: Truck,
  },
]);
</script>
