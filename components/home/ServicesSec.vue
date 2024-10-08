<template>
  <section id="services" class="relative overflow-hidden">
    <div class="container max-w-[1200px] my-20">
        <h2 class="text-4xl md:text-6xl font-extrabold text-center mb-12 relative z-10">
          Services We Offer
        </h2>
      <div class="max-w-[1200px] h-full bg-[url('/block.png')]">
        <div
          class="absolute inset-0 flex-none overflow-hidden z-2 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]  "
        ></div>
        <div class="relative">
          <div class="grid grid-cols-3 gap-y-[50px] gap-x-[66px]">
            <div
              v-for="(service, index) in services"
              :key="index"
              class="border  p-6 bg-background z-10 w-[350px] h-[400px]"
            >
              <div class="flex items-center"> 
                <h3 class="text-xl font-bold">
                  {{ service.title }}
                </h3>
              </div>
              <p class="my-4">{{ service.description }}</p>
              <Button class="rounded-full gap-2 px-20"
                >Learn More <ChevronRight size="16"
              /></Button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import { ChevronRight } from "lucide-vue-next";
const services = ref([
  {
    title: "UI/UX Design",
    description:
      "People subconciously see and respond to design first, functiontionality after. We offer design services that will make your final product user-friendly as well as visually appealing. Contact us to get well thought out interfaces to communicate and attract customers better.",
  },
  {
    title: "Business Management Consultation",
    description:
      "Hire in the expertise you need to structure, organize and automate the costly manual business processes. Our research based and goal driven approach in consulting, helps companies lay the perfect strategy. Get help in identifying friction points which can be solved programmatically and systematically.",
  },

  {
    title: "Financial & Technical Consulting",
    description:
      "Connectivo bridges the gap between accounting and entrepeneurship - we find accounting and business economics fun and interesting! Our financial plans & analytical reports help business owners, accountants, controllers and managers marshall their company resources sustainably.",
  },
  {
    title: "Security",
    description:
      "Employee’s and Data are the modern companies most important and valuable assets and should be treated as such. Our philosophy centers around securing and protecting our clients data. We store as little of your data as possible to achieve the results needed always using best practices and advanced encryption standards.",
  },
  {
    title: "Custom Software Development",
    description:
      "Our focused approach and project execution processes help set the right foundation for your unique machinery. Regardless if your systems/apps are stuck in the old, the new or in the middle, we manage to connect the dots. The data transfer protocol whether it be SFTP, API, SOAP, XML or REST, matters not.",
  },
  {
    title: "Standardized solutions",
    description:
      "Often as humans and organisations, we share the same problems. By offering standardized SaaS services, Connectivo aim to help and empower those on their digital journey. We simply produce standard solutions for common problems.",
  },
]);
</script>
