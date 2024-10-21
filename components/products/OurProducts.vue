<template>
  <div class="container mx-auto py-[160px]">
    <div
      class="mx-auto bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 text-xl font-bold w-fit px-6 flex items-center justify-center mb-4"
    >
      Discover
    </div>
    <h1
      class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold text-center"
    >
      <span class="text-primary">Our</span> Products
    </h1>

    <div class="flex gallery">
      <div class="left w-1/2">
        <div class="desktopContent mx-auto w-4/5">
          <div
            class="desktopContentSection min-h-screen flex flex-col justify-center"
            v-for="(product, x) in products"
            :key="x"
          >
            <h6 class="text-base font-semibold text-gray-400 mb-4">
              The AI-ready iPaaS
            </h6>
            <h1 class="text-4xl lg:text-6xl mb-6 font-semibold">
              {{ product.title }}
            </h1>
            <p class="text-xl leading-relaxed">
              {{ product.description }}
            </p>
            <a :href="product.url" target="_blank" class="mt-4">
              <Button class="font-bold">View More</Button>
            </a>
          </div>
        </div>
      </div>

      <div class="right w-1/2 h-screen flex flex-col justify-center">
        <div
          class="desktopPhotos relative w-[40vw] h-[40vw] rounded-2xl overflow-hidden shadow-lg"
        >
          <div
            class="desktopPhoto bg-gradient-to-r from-pink-500 via-red-500 to-orange-500 bg-crimson absolute inset-0 flex items-center justify-center"
            :class="product.color"
            v-for="(product, x) in products"
            :key="x"
          >
            <img :src="product.logo" :alt="product.title" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { DotLottieVue } from "@lottiefiles/dotlottie-vue";

export default {
  components: { DotLottieVue },
  data() {
    return {
      lottieTriggers: [],
      showLottie: false,
      products: [
        {
          title: "Automatisera Mera",
          description:
            "Automatisera Mera translates to Automate More and is a integrationsplatform specialized in automating the bookkeeping of business transactions. Started in 2019, the platform has grown into supporting 40 + integrations and 4+ Accounting ERPs.By providing affordable yet advanced app integrations accountants and business owners can easily plugin and start benefiting substantially in from the time and work savings of automated bookkeeping.",
          url: "https://automatiseramera.se/",
          color: "bg-gradient-to-r from-green-500 via-emerald-500 to-teal-500",
          logo: "/integration/sap.png",
        },
        {
          title: "B2B Portal",
          description:
            "B2B commerce is growing steadily year by year yet the market for apps and services to aid businesses in their B2B sales are still lacking in areas. After continous requests from our customers we decided to tackle the problem and build a platform which allows for the wholeseller to within minutes setup a wholesale shop, fully hosted and secured, and start inviting their resellers for placing purchase orders. As fan’s of automation, naturally we went ahead and integrated it with Fortnox, allowing for full invoicing automation.",
          url: "https://b2bportal.se/",
          color: "bg-gradient-to-r from-cyan-700 via-blue-500 to-indigo-600",
          logo: "/integration/sap.png",
        },
        {
          title: "Likvio",
          description:
            "ALikvio is a platform for businesses who use Fortnox and want to collect their financial data, statistics and recurring revenue analytics in an easy-to-navigate and highly functional portal, allwing business ownners to more easily visualize their financial data.",
          url: "https://likvio.se/",
          color: "bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500",
          logo: "/integration/sap.png",
        },
        {
          title: "Imexta",
          description:
            "Imexta is an import & export tool for moving data to and from financial programs such as Visma and Fortnox. With a few clicks, create completely custom templates that allow you to import/export specifically the data you need, where you need it.",
          url: "https://imexta.se/",
          logo: "/integration/sap.png",
          color: "bg-gradient-to-r from-green-500 via-emerald-500 to-teal-500",
        },
        {
          title: "Snabbskan",
          description:
            "Snabbskan is an simple to use app which helps customers skan their account statetments from creditcard to automate the bookkeeping of expenses in accounting apps such as Visma and Fortnox. With a few clicks, snabbskan helps you bookkeep endless amount of transactions in the ledger in seconds.",
          url: "https://snabbskan.se/",
          logo: "/integration/sap.png",
          color: "bg-gradient-to-r from-gray-600 via-blue-500 to-cyan-400",
        },
        {
          title: "Golfigo",
          description:
            "Connectivo have been providing accounting integrations for the Swedish Golf Associations members since 2019. Golfigo is the new upgraded platform with better features combined with more intutitive design.Golfigo integrates with Fortnox, Visma Admin and Visma eaccounting.",
          url: "https://golfigo.se/",
          logo: "/integration/sap.png",
          color: "bg-gradient-to-r from-blue-500 via-cyan-500 to-teal-500",
        },
        {
          title: "Duplio",
          description:
            "Duplio acts as a watcher robot that automatically identifies and notifies of duplicates in your accounting software, assisting in keeping your bookkeping accurate,free from duplicate posts and freeing time which would otherwise be spent searching for discrepancies. Duplio can be customized to deduplicate other entities such as CRM and Invoicing apps.",
          url: "https://duplio.se/",
          logo: "/integration/sap.png",
          color: "bg-gradient-to-r from-pink-200 via-rose-400 to-red-600",
        },
        {
          title: "Autofaktura",
          description:
            "AutoFaktura does one thing and that thing well. It helps companies who use Fortnox invoicing and need to have the invoices bookkept or sent to customers based on custom rules. AutoFaktura allows you to control which invoices are posted, which are sent directly to the customer and which are sent via Fortnox Fakturaserice.",
          url: "https://autofaktura.com/",
          logo: "/integration/sap.png",
          color: "bg-gradient-to-r from-blue-500 via-cyan-500 to-teal-500",
        },
      ],
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    this.createSectionScroll();
  },
  methods: {
    createSectionScroll() {
      const details = gsap.utils.toArray(
        ".desktopContentSection:not(:first-child)"
      );
      const photos = gsap.utils.toArray(".desktopPhoto:not(:first-child)");
      const allPhotos = gsap.utils.toArray(".desktopPhoto");
      gsap.set(photos, { yPercent: 101 });

      ScrollTrigger.create({
        trigger: ".gallery",
        start: "top top",
        end: "bottom bottom",
        pin: ".right",
        markers: false,
      });

      details.forEach((detail, index) => {
        let headline = detail.querySelector("h1");
        let animation = gsap
          .timeline()
          .to(photos[index], { yPercent: 0 })
          .set(allPhotos[index], { autoAlpha: 0 });
        ScrollTrigger.create({
          trigger: headline,
          start: "top 80%",
          end: "top 50%",
          markers: false,
          animation: animation,
          scrub: true,
        });
      });
    },
  },
};
</script>
