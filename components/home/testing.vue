<template>
  <div id="platform-integration" class="container mx-auto md:py-[160px] py-10">
    <div
      class="md:mx-auto bg-gradient-to-b from-[#2a462b8a] via-[#101010] border border-green-900 rounded-full p-2 md:text-xl font-bold w-fit px-6 flex items-center justify-center mb-4"
    >
      Discover
    </div>
    <h1
      class="text-4xl sm:text-5xl md:text-6xl lg:text-8xl font-bold text-center"
    >
      <span class="text-primary">Platform</span> Integrations
    </h1>
    <p class="mt-10 md:mb-20 max-w-5xl md:text-center mx-auto">
      Integration Platform as a Service (iPaaS) is a suite of cloud services,
      enabling companies to set up the synchronization of data between
      applications and configure specific workflow rules. We offer custom
      development kits for linking legacy or new applications with each other.
      Popular requested features from our clients include capabilities for
      managing, harvesting, and visualizing data.
    </p>
    <div class="flex gallery ">
      <div class="left md:w-1/2 w-auto">
        <div class="desktopContent mx-auto md:w-4/5">
          <div
            class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
          >
            <h6 class="text-base font-semibold text-gray-400 mb-4">
              The AI-ready iPaaS
            </h6>
            <h1 class="text-4xl sm:text-5xl md:text-6xl mb-6 font-semibold">
              10x faster results
            </h1>
            <p class="md:text-xl leading-relaxed">
              Accelerate integration and automation delivery with a powerful
              low-code, AI-augmented builder for business technologists and
              development teams.
            </p>
          </div>
          <div
            class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
          >
            <div
              class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
            >
              <h6 class="text-base font-semibold text-gray-400 mb-4">
                The AI-ready iPaaS
              </h6>
              <h1 class="text-4xl sm:text-5xl md:text-6xl mb-6 font-semibold">
                10x faster results
              </h1>
              <p class="md:text-xl leading-relaxed">
                Accelerate integration and automation delivery with a powerful
                low-code, AI-augmented builder for business technologists and
                development teams.
              </p>
            </div>
          </div>
          <div
            class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
          >
            <div
              class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
            >
              <h6 class="text-base font-semibold text-gray-400 mb-4">
                The AI-ready iPaaS
              </h6>
              <h1 class="text-4xl sm:text-5xl md:text-6xl mb-6 font-semibold">
                10x faster results
              </h1>
              <p class="md:text-xl leading-relaxed">
                Accelerate integration and automation delivery with a powerful
                low-code, AI-augmented builder for business technologists and
                development teams.
              </p>
              <p class="md:text-xl leading-relaxed">
                Accelerate integration and automation delivery with a powerful
                low-code, AI-augmented builder for business technologists and
                development teams.
              </p>
            </div>
          </div>
          <div
            class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
          >
            <div
              class="desktopContentSection md:min-h-screen my-6 md:my-0 flex flex-col justify-center"
            >
              <h6 class="text-base font-semibold text-gray-400 mb-4">
                The AI-ready iPaaS
              </h6>
              <h1 class="text-4xl sm:text-5xl md:text-6xl mb-6 font-semibold">
                10x faster results
              </h1>
              <p class="md:text-xl leading-relaxed">
                Accelerate integration and automation delivery with a powerful
                low-code, AI-augmented builder for business technologists and
                development teams.
              </p>
              <p class="md:text-xl leading-relaxed mt-3">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Commodi, sit facere magni, totam laborum error obcaecati, odio
                tempore placeat nulla asperiores nisi. Repellendus reprehenderit
                ipsa officiis consequatur, aperiam laborum a?
              </p>
              <p class="md:text-xl leading-relaxed mt-3">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Commodi, sit facere magni, totam laborum error obcaecati, odio
                tempore placeat nulla asperiores nisi. Repellendus reprehenderit
                ipsa officiis consequatur, aperiam laborum a?
              </p>
            </div>
          </div>
        </div>
      </div>

      <div class="right w-1/2 h-screen  flex-col justify-center hidden md:flex">
        <div
          class="desktopPhotos relative w-[40vw] h-[40vw] rounded-2xl overflow-hidden shadow-lg"
        >
          <div
            class="desktopPhoto bg-gradient-to-r from-pink-500 via-red-500 to-orange-500 bg-crimson absolute inset-0 flex items-center justify-center"
          >
            <DotLottieVue
              v-if="showLottie"
              style="height: 500px; width: 500px"
              autoplay
              loop
              src="https://assets.ctfassets.net/7rbn0raz0t75/6S4XdJkUf7h3JB2DHkVyub/8809626e8a9a8cf656fc95d28ba26b62/Composable_AI_Integration_Platform.json"
            />
          </div>
          <div
            class="desktopPhoto flex items-center justify-center bg-[linear-gradient(60deg,_rgb(247,_149,_51),_rgb(243,_112,_85),_rgb(239,_78,_123),_rgb(161,_102,_171),_rgb(80,_115,_184),_rgb(16,_152,_173),_rgb(7,_179,_155),_rgb(111,_186,_130))] bg-mediumseagreen absolute inset-0"
          >
            <DotLottieVue
              v-if="lottieTriggers[0]"
              style="height: 500px; width: 500px"
              autoplay
              loop
              src="https://assets.ctfassets.net/7rbn0raz0t75/6Ryl6nYRduf9osSml8o55G/fee72abfb0a6f12d433c7afb4f71b423/10x_Faster_Results.json"
            />
          </div>
          <div
            class="desktopPhoto flex items-center justify-center bg-gradient-to-br from-gray-800 via-blue-700 to-gray-900 bg-deeppink absolute inset-0"
          >
            <DotLottieVue
              v-if="lottieTriggers[1]"
              style="height: 500px; width: 500px"
              autoplay
              loop
              src="https://assets.ctfassets.net/7rbn0raz0t75/3GaesFQuhBNUetIRxkbqTA/d4056b27b9add6b4389e0e8dc941a442/Infuse_AI_Into_Business.json"
            />
          </div>
          <div
            class="desktopPhoto flex items-center justify-center bg-gradient-to-r from-cyan-100 via-blue-300 to-indigo-400 bg-dodgerblue absolute inset-0"
          >
            <DotLottieVue
              v-if="lottieTriggers[2]"
              style="height: 500px; width: 500px"
              autoplay
              loop
              src="https://assets.ctfassets.net/7rbn0raz0t75/90lqGdCclqKpsTshc6Qne/e69004681d855df31eae0f7ace5219e7/Trusted_AI_Integration.json"
            />
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
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    this.sectionEnter();
    this.createSectionScroll();
  },
  methods: {
    sectionEnter() {
      ScrollTrigger.create({
        trigger: "#platform-integration",
        start: "top top",
        onEnter: () => {
          this.showLottie = true;
          console.log("Container in view, Lottie animation triggered!");
        },
        markers: false,
      });
    },
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
          onEnter: () => this.triggerLottieAnimations(index),
          scrub: true,
        });

        this.lottieTriggers.push(false);
      });
    },
    triggerLottieAnimations(index) {
      this.lottieTriggers[index] = true;
    },
  },
};
</script>
