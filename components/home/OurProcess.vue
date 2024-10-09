<template>
  <section id="process" class="container md:py-[150px]">
    <h2
      class="text-center md:text-start text-4xl md:text-6xl font-extrabold relative z-10"
    >
      Our Process
    </h2>

    <div class="overflow-hidden mt-12">
      <div
        v-for="(service, index) in services"
        :key="index"
        class="border-b py-10"
      >
        <div class="md:flex gap-10">
          <h1
            class="text-7xl hidden md:block md:text-9xl font-extrabold text-neutral-700"
          >
            {{ index + 1 }}.
          </h1>
          <div>
            <h3 class="text-4xl font-bold">{{ service.title }}</h3>
            <p class="text text-gray-400 mt-6">
              {{ service.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const services = ref([
  {
    title: "Development Plan & Production",
    description:
      "With an accepted offer and agreed upon strategy, the craftsmanship starts to convert ideas, needs, and demands from concept to code. Each project is led by a minimum of one project manager and, depending on the client's budget, one or several seasoned developers. Our experience in custom application development has contributed to the formation and growth of companies in a variety of industries. Every developer in our team understands that clients depend on the quality of their work and thus put all efforts to give the best result possible.",
  },
  {
    title: "Situation and strategy analysis",
    description:
      "There's a lot that we do before actually starting the project. Market research and analysis, studying and understanding the technical documentation to assess the limitations and possibilities between apps, listening in on the clients’ needs and preferences, consulting with stakeholders, and finally coming up with a high-level mapping. With emphasis on planning and problem solving, the client can expect to receive a clear execution plan.",
  },
  {
    title: "Delivery & Follow-up",
    description:
      "After close contact and careful development, delivery of the product/service follows. A quality review is done to see that everything is up to standard. Should any errors or bumps still creep in, we have a guarantee that covers errors discovered within 30 days of delivery free of charge to ensure the client's needs are met.",
  },
]);
</script>
