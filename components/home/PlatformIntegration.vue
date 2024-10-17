<template>
  <section
    class="relative text-white p-8 md:pt-[350px] md:pb-[150px] overflow-hidden"
  >
    <div
      class="absolute inset-0 -z-10 transform -skew-y-6 origin-right"
      style="background: linear-gradient(to bottom, #0d1117, black, #1e2368)"
    >
      <div class="bg-primary w-[500px] h-12 absolute left-0 -top-[50px]">
        <div
          class="bg-[#2176e4b4] w-[250px] h-12 absolute left-[180px] -top-[30px]"
        ></div>
      </div>
    </div>
    <div class="container z-10">
      <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold">
        <span class="text-primary">Platform</span> Integrations
      </h1>
      <p class="mt-10 mb-20 max-w-5xl">
        Integration Platform as a Service (iPaaS) is a suite of cloud services,
        enabling companies to set up the synchronization of data between
        applications and configure specific workflow rules. We offer custom
        development kits for linking legacy or new applications with each other.
        Popular requested features from our clients include capabilities for
        managing, harvesting, and visualizing data.
      </p>
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <div
          v-for="logo in logos"
          :key="logo.name"
          class="bg-white rounded-2xl p-4 flex items-center justify-center hover:bg-opacity-80 transition-all duration-300 transform hover:scale-105"
        >
          <img :src="logo.src" :alt="logo.name" class="max-h-12" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const logos = [
  { name: "Visma", src: "/integration/visma.png" },
  { name: "SAP", src: "/integration/sap.png" },
  { name: "Chargebee", src: "/integration/chargebee.png" },
  { name: "Shopify", src: "/integration/shopify.png" },
  { name: "Zoho", src: "/integration/zoho.png" },
  { name: "Odoo", src: "/integration/odoo.png" },
  { name: "Fortnox", src: "/integration/fortnox.png" },
  { name: "Pipedrive", src: "/integration/pipedrive.png" },
  { name: "Salesforce", src: "/integration/salesforce.png" },
  { name: "G Suite", src: "/integration/g-suite.png" },
  { name: "Oracle", src: "/integration/oracle.png" },
  {
    name: "Microsoft Dynamics 365",
    src: "/integration/microsoft365.png",
  },
];
</script>
