<template>
  <section id="IntegrationsSection" class="container py-[150px]">
    <h1 class="text-3xl md:text-6xl font-extrabold mb-6 leading-tight">
      Platform integrations
    </h1>
    <p class="text-gray-400 text-lg">
      Integration Platform as a Service (iPaaS) is a suite of cloud services,
      enabling companies to set up the synchronization of data between
      applications and configure specific workflow rules. Connectivo offers
      custom development kits for linking legacy or new applications with each
      other. Popular requested features from our previous clients include
      capabilities for managing, harvesting, and visualizing data.
    </p>
    <div class="mt-10">
      <div v-for="(skillGroup, index) in skillGroups" :key="index">
        <div class="mt-2">
          <div>
            <Vue3Marquee
              class="skills overflow-hidden"
              :direction="index % 2 === 0 ? 'reverse' : 'normal'"
            >
              <div
                v-for="(skill, skillIndex) in repeatedSkills(skillGroup)"
                :key="skillIndex"
                class="flex items-center space-x-4"
              >
                <img
                  v-if="skill.img"
                  :src="skill.img"
                  alt=""
                  class="w-32 mr-40 py-5 filter brightness-150"
                />
              </div>
            </Vue3Marquee>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { Vue3Marquee } from "vue3-marquee";
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
  components: {
    Vue3Marquee,
  },
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
  computed: {
    skillGroups() {
      const skillsPerGroup = 4;
      const skillGroups = [];
      for (let i = 0; i < this.skills.length; i += skillsPerGroup) {
        skillGroups.push(this.skills.slice(i, i + skillsPerGroup));
      }
      return skillGroups;
    },
  },
  methods: {
    repeatedSkills(skillGroup) {
      // Repeat the skills for seamless scrolling
      return [...skillGroup, ...skillGroup]; // Duplicate the group
    },
  },
};
</script>
