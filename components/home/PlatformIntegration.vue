<template>
  <section
    id="IntegrationsSection"
    class="container p-8 md:py-20  md:my-[150px]"
  >
    <h1 class="md:text-7xl text-4xl font-bold mb-20 text-center">
      Platform <span class="text-primary">Integrations</span>
    </h1>
    <p class="text-gray-400 text-lg">
      Integration Platform as a Service (iPaaS) is a suite of cloud services,
      enabling companies to set up the synchronization of data between
      applications and configure specific workflow rules. Connectivo offers
      custom development kits for linking legacy or new applications with each
      other. Popular requested features from our previous clients include
      capabilities for managing, harvesting, and visualizing data.
    </p>

    <div class="grid grid-cols-2 md:grid-cols-4 gap-10 mt-10">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="flex items-center justify-center"
      >
        <img
          v-if="skill.img"
          :src="skill.img"
          alt="Integration Logo"
          class="w-32 py-5 filter brightness-150"
        />
      </div>
    </div>
  </section>
</template>

<script>
import sap from "/integration/sap.png";
import odoo from "/integration/odoo.png";
import shopify from "/integration/shopify.png";
import chargebee from "/integration/chargebee.png";
import fortnox from "/integration/fortnox.png";
import gsuite from "/integration/g-suite.png";
import microsoft365 from "/integration/microsoft365.png";
import oracle from "/integration/oracle.png";
import pipedrive from "/integration/pipedrive.png";
import salesforce from "/integration/salesforce.png";
import visma from "/integration/visma.png";
import zoho from "/integration/zoho.png";

export default {
  data() {
    return {
      skills: [
        { img: sap },
        { img: odoo },
        { img: shopify },
        { img: chargebee },
        { img: fortnox },
        { img: gsuite },
        { img: microsoft365 },
        { img: oracle },
        { img: pipedrive },
        { img: salesforce },
        { img: visma },
        { img: zoho },
      ],
    };
  },
};
</script>
