<template>
  <div class="bg-gray-900 text-white py-16 px-4">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-3xl font-bold mb-4 text-center">Integrations and Extensibility</h2>
      <p class="text-gray-400 text-center mb-12 max-w-2xl mx-auto">
        Integrate seamlessly with social media platforms for automatic posting and interaction analysis,
        and extend functionality through plugins and APIs for analytics and email marketing.
      </p>
      
      <div class="grid grid-cols-5 gap-8 mb-12">
        <div v-for="integration in integrations" :key="integration.name" class="flex flex-col items-center">
          <div class="bg-gray-800 rounded-full p-4 mb-2">
            <img :src="integration.image" alt="" class="w-8 h-8" />
          </div>
          <span class="text-sm text-gray-400">{{ integration.name }}</span>
        </div>
      </div>
      
      <div class="text-center">
        <button class="bg-gray-800 text-white px-6 py-3 rounded-full hover:bg-gray-700 transition-colors duration-300">
          Show all integrations
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import odoo from "/assets/img/odoo.png";
import chargebee from "/assets/img/chargebee.png";
import fortnox from "/assets/img/fortnox.png";
import Gsuite from "/assets/img/g-suite.png";
import microsoft365 from "/assets/img/microsoft365.png";
import oracle from "/assets/img/oracle.png";
import pipedrive from "/assets/img/pipedrive.png";
import salesforce from "/assets/img/salesforce.png";
import sap from "/assets/img/sap.png";
import shopify from "/assets/img/shopify.png";
import visma from "/assets/img/visma.png";
import zoho from "/assets/img/zoho.png";

const integrations = [
  { name: 'Odoo', image: odoo },

]
</script>
