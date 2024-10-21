<template>
  <div
    class="text-card-foreground md:min-h-screen flex items-center justify-center"
  >
    <div
      class="w-full mx-auto text-center bg-[url('/block.png')] overflow-hidden py-[100px] md:px-20 relative"
    >
      <div
        class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]"
      ></div>
      <div class="z-2 relative">
        <div class="container md:grid md:grid-cols-2">
          <div class="text-start">
            <h1
              class="text-3xl text-center md:text-start md:text-6xl font-extrabold md:mb-6 mb-2 leading-tight"
            >
              Standard solutions for common problems.
            </h1>
            <p
              class="text-lg text-center md:text-start md:text-2xl text-gray-400 mb-4 md:mb-10 max-w-3xl auto"
            >
              SaaS services built to empower companies and accelerate their
              digital journey.
            </p>
            <div class="md:space-x-4 flex flex-col items-center md:block">
              <router-link :to="{ path: '/products', hash: '#contact' }">
                <Button size="sm" class="rounded-full gap-2 h-7">
                  Contact Us <ChevronRight size="16" />
                </Button>
              </router-link>

              <router-link :to="{ path: '/', hash: '#services' }">
                <Button
                  size="sm"
                  class="rounded-full gap-2 h-7 hover:bg-background hover:underline border-0 mt-4 md:mt-0"
                  variant="outline"
                  >View Custom Software Services <ChevronRight size="16"
                /></Button>
              </router-link>
            </div>
          </div>
          <div class=""></div>
          <div class=""></div>
          <div
            class="md:border rounded-2xl text-start bg-background p-6 md:outline outline-2 outline-orange-800 outline-offset-[6px] mt-10 md:-mt-[150px] md:ml-10 ms-auto"
          >
            <h1 class="text-2xl font-bold flex gap-4">
              <MessageCircleMore class="mt-2 hidden md:block" />
              Entrepeneurship is tough. We are here to make it easier.
            </h1>
            <p class="mt-2 mx-auto text-gray-500 md:pl-9">
              Connectivo was founded in 2013 and spent the first 4 years of
              trade in e-commerce, selling in a variety of countries and
              marketplaces. We found early on a variety of friction points and
              time-consuming manual steps which prevented us from realizing the
              target goals. With every problem, a bigger solution can be found.
              After some years of frustration, we decided to drop what we were
              doing and get to the root of the problem.
            </p>

            <p v-if="showMore" class="mt-2 mx-auto text-gray-500 pl-9">
              With a background in IT, accounting, e-commerce, finance and
              business development we merged all experiences together and
              started designing and coding software solutions to help push
              entrepreneurs forward. Today, Connectivo provides standardized
              apps and platforms that solve common problems within a variety of
              industries.
              <br />
              The company is 100% founder-owned, profitable, and fully
              bootstrapped. This allows us to continuously put our clients'
              needs above all without compromising on quality, mission, or
              vision.
            </p>

            <Button
              @click="toggleShowMore"
              class="mt-4 md:ml-9 bg-background px-0 text-primary hover:bg-background hover:underline"
            >
              {{ showMore ? "Show Less" : "Show More" }}
            </Button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="container">
    <h1 class="text-4xl font-bold text-center mb-12 text-gray-800">
      Our Products
    </h1>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div
        v-for="(product, index) in products"
        :key="index"
        class="bg-white rounded-lg shadow-lg overflow-hidden transform transition duration-300 hover:scale-105"
      >
        <div :class="[product.color, 'h-2']"></div>
        <div class="p-6">
          <img
            :src="product.logo"
            :alt="product.title"
            class="w-20 h-20 mb-4 mx-auto"
          />
          <h2 class="text-2xl font-semibold text-gray-800 mb-2">
            {{ product.title }}
          </h2>
          <p class="text-gray-600 mb-4">{{ product.description }}</p>
          <button
            class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
          >
            See more
            <ChevronRight class="ml-2 -mr-1 h-4 w-4" aria-hidden="true" />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import { ChevronRight, MessageCircleMore } from "lucide-vue-next";

const products = ref([
  {
    title: "Automatisera Mera",
    description:
      "Automatisera Mera translates to Automate More and is a integrationsplatform specialized in automating the bookkeeping of business transactions. Started in 2019, the platform has grown into supporting 40 + integrations and 4+ Accounting ERPs.By providing affordable yet advanced app integrations accountants and business owners can easily plugin and start benefiting substantially in from the time and work savings of automated bookkeeping.",
    url: "https://automatiseramera.se/",
    color: "bg-emerald-500",
    logo: "/placeholder.svg?height=80&width=80",
  },
  {
    title: "B2B Portal",
    description:
      "B2B commerce is growing steadily year by year yet the market for apps and services to aid businesses in their B2B sales are still lacking in areas. After continous requests from our customers we decided to tackle the problem and build a platform which allows for the wholeseller to within minutes setup a wholesale shop, fully hosted and secured, and start inviting their resellers for placing purchase orders. As fan’s of automation, naturally we went ahead and integrated it with Fortnox, allowing for full invoicing automation.",
    url: "https://b2bportal.se/",
    color: "bg-blue-500",
    logo: "/placeholder.svg?height=80&width=80",
  },
  {
    title: "Likvio",
    description:
      "ALikvio is a platform for businesses who use Fortnox and want to collect their financial data, statistics and recurring revenue analytics in an easy-to-navigate and highly functional portal, allwing business ownners to more easily visualize their financial data.",
    url: "https://likvio.se/",
    color: "bg-purple-500",

    logo: "/placeholder.svg?height=80&width=80",
  },
  {
    title: "Imexta",
    description:
      "Imexta is an import & export tool for moving data to and from financial programs such as Visma and Fortnox. With a few clicks, create completely custom templates that allow you to import/export specifically the data you need, where you need it.",
    url: "https://imexta.se/",
  },
  {
    title: "Snabbskan",
    description:
      "Snabbskan is an simple to use app which helps customers skan their account statetments from creditcard to automate the bookkeeping of expenses in accounting apps such as Visma and Fortnox. With a few clicks, snabbskan helps you bookkeep endless amount of transactions in the ledger in seconds.",
    url: "https://snabbskan.se/",
  },
  {
    title: "Golfigo",
    description:
      "Connectivo have been providing accounting integrations for the Swedish Golf Associations members since 2019. Golfigo is the new upgraded platform with better features combined with more intutitive design.Golfigo integrates with Fortnox, Visma Admin and Visma eaccounting.",
    url: "https://golfigo.se/",
  },
  {
    title: "Duplio",
    description:
      "Duplio acts as a watcher robot that automatically identifies and notifies of duplicates in your accounting software, assisting in keeping your bookkeping accurate,free from duplicate posts and freeing time which would otherwise be spent searching for discrepancies. Duplio can be customized to deduplicate other entities such as CRM and Invoicing apps.",
    url: "https://duplio.se/",
  },
  {
    title: "Autofaktura",
    description:
      "AutoFaktura does one thing and that thing well. It helps companies who use Fortnox invoicing and need to have the invoices bookkept or sent to customers based on custom rules. AutoFaktura allows you to control which invoices are posted, which are sent directly to the customer and which are sent via Fortnox Fakturaserice.",
    url: "https://autofaktura.com/",
  },
]);
// Reactive state to track if the "Show More" is toggled
const showMore = ref(false);

// Function to toggle the "Show More" state
const toggleShowMore = () => {
  showMore.value = !showMore.value;
};
</script>
