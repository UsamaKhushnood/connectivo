<template>
  <div
    class="min-h-[800px] h-screen flex flex-col justify-center text-white p-4 sm:p-8 bg-[url('/public/bg-green.png')] bg-center bg-cover sm:bg-contain bg-no-repeat sm:bg-right bg-black -mt-[55px]"
  >
    <div class="container mx-auto">
      <div
        class="bg-[#1a3c2587] px-3 py-2 border-2 border-green-800 text-xs sm:text-sm rounded-full w-fit flex items-center gap-2 sm:gap-3 mx-auto mb-8 sm:mb-12 md:mb-20 whitespace-nowrap"
      >
        <div class="px-2 py-1 text-[10px] sm:text-xs bg-blue-700 rounded-full">New</div>
        <span class="text-xs sm:text-sm md:text-lg font-semibold uppercase">Your technology partner</span>
        <MoveRight class="w-4 h-4 sm:w-5 sm:h-5" />
      </div>
      <div class="mx-auto w-fit text-center mb-16 sm:mb-20 md:mb-[120px]">
        <div class="text-start">
          <div
            class="flex gap-2 sm:gap-3 items-center font-extrabold text-3xl sm:text-4xl md:text-6xl lg:text-8xl justify-center"
          >
            <h1 class="whitespace-pre">Connect the</h1>
            <div
              class="text-primary inline-flex flex-col overflow-hidden"
              :class="{
                'h-[calc(theme(fontSize.3xl)*theme(lineHeight.tight))]': true,
                'sm:h-[calc(theme(fontSize.4xl)*theme(lineHeight.tight))]': true,
                'md:h-[calc(theme(fontSize.6xl)*theme(lineHeight.tight))]': true,
                'lg:h-[calc(theme(fontSize.8xl)*theme(lineHeight.tight))]': true,
              }"
            >
              <ul
                class="block animate-text-slide-5 text-left leading-tight [&_li]:block"
              >
                <li>Dots</li>
                <li>Tech</li>
                <li>Dots</li>
                <li>Tech</li>
                <li>Dots</li>
                <li aria-hidden="true">Dots</li>
              </ul>
            </div>
          </div>
        </div>

        <p class="text-base sm:text-lg md:text-xl mb-6 sm:mb-8 text-center max-w-xl sm:max-w-2xl mx-auto">
          Free up your time by connecting the systems you depend on, by a
          provider you can count on.
        </p>
        <!-- Uncomment and adjust as needed
        <div class="flex flex-col sm:flex-row gap-4 items-center justify-center">
          <Button
            class="w-full sm:w-auto font-semibold text-sm sm:text-base hover:bg-secondary hover:text-white"
          >
            Take interactive tour
          </Button>
          <Button
            class="w-full sm:w-auto font-semibold text-sm sm:text-base bg-white hover:bg-primary"
          >
            Talk to us
          </Button>
        </div>
        -->
      </div>
      <!-- Uncomment and adjust as needed
      <div>
        <TheCard
          class="p-6 sm:p-8 md:p-10 rounded-2xl sm:rounded-3xl mb-8 sm:mb-12 max-w-xl sm:max-w-2xl mt-6 sm:mt-10 text-start bg-black mx-auto"
        >
          <h3 class="text-xl sm:text-2xl md:text-3xl font-bold mb-2 capitalize">
            Your technology partner for digital solutions.
          </h3>
          <p class="text-xs sm:text-sm text-gray-300">
            Connectivo assists SME companies in optimizing, connecting, and
            improving their business processes. We are small enough to see,
            listen, and care about our customers' success, yet big enough to
            engage, push, and deliver software that allows businesses to reach
            their target goals.
          </p>
        </TheCard>
      </div>
      -->
    </div>
  </div>
</template>

<script setup>
import { MoveRight } from "lucide-vue-next";
import TheCard from "@/components/common/TheCard.vue";
</script>