<template>
  <div
    class="text-card-foreground flex items-center justify-center bg-green-50 text-black"
  >
    <div
      class="w-full mx-auto text-center overflow-hidden md:py-[100px] md:px-20 relative"
    >
      <!-- <div
        class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(4_44_42)_100%)]"
      ></div> -->
      <div class="z-2 relative">
        <div class="flex justify-center">
          <div class="border rounded-full px-3 shadow text-black">
            Power of Saas
          </div>
        </div>
        <div
          class="container max-w-[1360px] mx-auto md:flex md:pt-20 pb-2 text-black"
        >
          <div class="text-start">
            <div
              class="flex gap-3 items-center font-extrabold text-4xl md:text-6xl"
            >
              <h1 class="whitespace-pre">Connect the</h1>
              <div
                class="text-secondary inline-flex flex-col min-h-[calc(theme(fontSize.6xl)*theme(lineHeight.tight))] md:h-[calc(theme(fontSize.4xl)*theme(lineHeight.tight))] overflow-hidden"
              >
                <ul
                  class="block animate-text-slide-5 text-left leading-tight [&_li]:block"
                >
                  <li>Dots</li>
                  <li>Tech</li>
                  <li>AI</li>
                  <li>Crypto</li>
                  <li>AI</li>

                  <li aria-hidden="true">Dots</li>
                </ul>
              </div>
            </div>

            <p
              class="text-center md:text-start text-lg md:text-2xl mt-2 mb-4 md:mb-10 max-w-3xl auto"
            >
              Free up your time by connecting the systems you depend on, by a
              provider you can count on.
            </p>
            <div
              class="md:space-x-4 flex flex-col items-center md:block text-white"
            >
              <router-link to="/products">
                <Button size="sm" class="rounded-full gap-2 h-7"
                  >View Saas Products <ChevronRight size="16"
                /></Button>
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
            <div
              class="max-w-2xl shadow rounded-3xl text-start bg-blue-50 border border-secondary border-b-[6px] text-black md:p-6 mt-14 mr-14"
            >
              <h1
                class="text-2xl font-extrabold flex gap-2 md:text-start text-secondary"
              >
                Your technology partner for digital solutions.
              </h1>
              <p class="mt-2 mx-auto md:text-start">
                Connectivo assists SME companies in optimizing, connecting, and
                improving their business processes. We are small enough to see,
                listen and care about our customers success, yet big enough to
                engage, push and deliver software which allows for businesses to
                reach their target goals.
              </p>
            </div>
          </div>
          <div class="pt-6">
            <div class="ms-auto max-w-lg">
              <div class="flex justify-center gap-3 mb-6">
                <div
                  class="uppercase text-sm rounded-full shadow bg-orange-200 font-bold px-3 py-1"
                >
                  Something
                </div>
                <div
                  class="uppercase text-sm rounded-full shadow bg-pink-200 font-bold px-3 py-1"
                >
                  Another thing
                </div>
                <div
                  class="uppercase text-sm rounded-full shadow bg-red-200 font-bold px-3 py-1"
                >
                  thing
                </div>
              </div>

              <img src="/floating-img.webp" />
              <div class="flex flex-wrap gap-10 mt-6">
                <Icon icon="skill-icons:wordpress" class="h-12 w-12" />
                <Icon icon="skill-icons:sass" class="h-12 w-12" />
                <Icon icon="logos:microsoft-icon" class="h-12 w-12" />
                <Icon icon="logos:google-calendar" class="h-12 w-12" />
                <Icon icon="logos:shopify" class="h-12 w-12" />
                <Icon icon="logos:google-drive" class="h-12 w-12" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ChevronRight, MessageCircleMore } from "lucide-vue-next";
import { Icon } from "@iconify/vue";
</script>
