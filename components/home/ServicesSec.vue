<template>
  <section>
    <div class="max-w-[1600px] mx-auto text-white p-8 md:py-[150px]">
      <div
        class="bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 text-xl font-bold w-fit px-6 flex items-center justify-center mb-4"
      >
        Discover
      </div>
      <h1
        class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold mb-10 sm:mb-16 md:mb-20"
      >
        <span class="text-primary">Services</span> We Offer
      </h1>
      <div class="grid grid-col-1 md:grid-cols-4 gap-6">
        <div
          v-for="(feature, index) in features"
          :key="index"
          :class="['col-span-1', getGridClass(index)]"
          class="md:w-[400px]"
        >
          <div
            class="md:mb-[50px] mb-5 bg-gradient-to-b from-[#101010] via-[#101010] to-[#000000] rounded-2xl border p-6 h-full flex flex-col justify-between"
          >
            <div
              class="bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 w-20 h-20 flex items-center justify-center mb-4"
            >
              <component :is="feature.icon" class="text-primary" size="30" />
            </div>
            <div>
              <h2 class="md:text-3xl text-2xl font-bold mb-2 text-white">
                {{ feature.title }}
              </h2>
              <p class="text-gray-400 flex-grow mt-6 text-sm md:text-base">
                {{ feature.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import {
  BriefcaseBusiness,
  Infinity,
  Code,
  BarChart,
  Lock,
  Grip,
} from "lucide-vue-next";

const features = [
  {
    icon: BriefcaseBusiness,

    title: "Business Management Consultation",
    description:
      "Hire in the expertise you need to structure, organize and automate the costly manual business processes. Our research based and goal driven approach in consulting, helps companies lay the perfect strategy. Get help in identifying friction points which can be solved programmatically and systematically.",
  },
  {
    icon: Infinity,

    title: "Custom Software Development",
    description:
      "Our focused approach and project execution processes help set the right foundation for your unique machinery. Regardless if your systems/apps are stuck in the old, the new or in the middle, we manage to connect the dots. The data transfer protocol whether it be SFTP, API, SOAP, XML or REST, matters not.",
  },

  {
    icon: Grip,

    title: "Standardized solutions",
    description:
      "Often as humans and organisations, we share the same problems. By offering standardized SaaS services, Connectivo aim to help and empower those on their digital journey. We simply produce standard solutions for common problems.",
  },

  {
    icon: Code,
    title: "UI/UX Design",
    description:
      "People subconciously see and respond to design first, functiontionality after. We offer design services that will make your final product user-friendly as well as visually appealing. Contact us to get well thought out interfaces to communicate and attract customers better.",
  },
  {
    icon: BarChart,

    title: "Financial & Technical Consulting",
    description:
      "Connectivo bridges the gap between accounting and entrepeneurship - we find accounting and business economics fun and interesting! Our financial plans & analytical reports help business owners, accountants, controllers and managers marshall their company resources sustainably.",
  },

  {
    icon: Lock,

    title: "Security",
    description:
      "Employee’s and Data are the modern companies most important and valuable assets and should be treated as such. Our philosophy centers around securing and protecting our clients data. We store as little of your data as possible to achieve the results needed always using best practices and advanced encryption standards.",
  },
];
const getGridClass = (index) => {
  switch (index) {
    case 0:
      return "md:col-start-1 md:row-start-1";
    case 1:
      return "md:col-start-3 md:row-start-1";
    case 2:
      return "md:col-start-2 md:row-start-2";
    case 3:
      return "md:col-start-4 md:row-start-2";
    case 4:
      return "md:col-start-1 md:row-start-3";
    case 5:
      return "md:col-start-3 md:row-start-3";
    default:
      return "";
  }
};
</script>
