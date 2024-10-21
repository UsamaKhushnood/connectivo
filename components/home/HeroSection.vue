<template>
  <div class="bg-[url('/block.png')] relative">
    <div
      class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]"
    ></div>
    <div
      class="relative min-h-[800px] h-screen flex flex-col justify-center text-white p-8 bg-center bg-[url('/public/green-bg.svg')] -mt-[55px]"
    >
      <div class="container">
        <div class="grid grid-cols-2">
          <div>
            <div
              class="bg-[#1a3c2587] pl-2 pr-4 py-2 border-2 border-green-800 text-sm rounded-full w-fit flex items-center gap-3"
            >
              <div class="px-2 py-1 text-xs bg-blue-700 rounded-full">New</div>
              <span class="font-semibold"> Free lifetime updates</span>
              <MoveRight />
            </div>
            <div class="text-start">
              <div
                class="flex gap-3 items-center font-semibold text-4xl md:text-7xl"
              >
                <h1 class="whitespace-pre">Connect the</h1>
                <div
                  class="text-primary font-extrabold inline-flex flex-col min-h-[calc(theme(fontSize.7xl)*theme(lineHeight.tight))] md:h-[calc(theme(fontSize.4xl)*theme(lineHeight.tight))] overflow-hidden"
                >
                  <ul
                    class="block animate-text-slide-5 text-left leading-tight [&_li]:block"
                  >
                    <li>Dots</li>
                    <li>Tech</li>
                    <li>AI</li>
                    <li>Tech</li>
                    <li>AI</li>

                    <li aria-hidden="true">Dots</li>
                  </ul>
                </div>
              </div>
            </div>

            <p class="text-xl mb-8 max-w-2xl">
              Free up your time by connecting the systems you depend on, by a
              provider you can count on.
            </p>
            <Button size="lg" class="rounded-full font-bold"
              >View Saas Products</Button
            >
            <Button size="lg" class="rounded-full font-bold ml-3"
              >Contact Us</Button
            >
          </div>
          <div class="relative min-h-[400px]">
            <img class="absolute -top-[150px]" src="/background.png" />
            <img
              width="200px"
              class="absolute top-0 right-0 animate-levitate z-40"
              src="/shape-2.png"
            />
            <img
              width="300px"
              class="absolute bottom-[-100px] animate-levitate right-[50px] z-10"
              src="/shape-1.png"
            />
            <div
              class="absolute max-w-md left-0 top-[120px] p-20 bg-gradient-to-b from-[#101010a9] via-[#171529] to-[#00000085] rounded-2xl z-30"
            >
              <h6 class="text-lg mb-2 capitalize leading-6 font-bold">
                Your technology partner for digital solutions.
              </h6>
              <p class="text-xs text-gray-300">
                Connectivo assists SME companies in optimizing, connecting, and
                improving their business processes. We are small enough to see,
                listen, and care about our customers' success, yet big enough to
                engage, push, and deliver software that allows businesses to
                reach their target goals.
              </p>
              <div
                class="px-2 py-1 text-xs bg-blue-700 rounded-full w-fit mt-4"
              >
                View Custom Software Services
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { MoveRight } from "lucide-vue-next";
import TheCard from "@/components/common/TheCard.vue";
</script>
