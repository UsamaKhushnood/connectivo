<template>
  <div
    class="min-h-[800px] h-screen flex flex-col justify-center text-white p-8 bg-[url('/public/bg-green.png')] bg-contain bg-no-repeat bg-right bg-black -mt-[55px]"
  >
    <div class="container">
      <div
        class="bg-[#1a3c2587] pl-2 pr-4 py-2 border-2 border-green-800 text-sm rounded-full w-fit flex items-center gap-3 mx-auto mb-20"
      >
        <div class="px-2 py-1 text-xs bg-blue-700 rounded-full">New</div>
        <span class="font-semibold uppercase"> Your technology partner </span>
        <MoveRight />
      </div>
      <div class="mx-auto w-fit text-center mb-[120px]">
        <div class="text-start">
          <div
            class="flex gap-3 items-center font-extrabold text-4xl md:text-8xl"
          >
            <h1 class="whitespace-pre">Connect the</h1>
            <div
              class="text-primary inline-flex flex-col min-h-[calc(theme(fontSize.8xl)*theme(lineHeight.tight))] md:h-[calc(theme(fontSize.4xl)*theme(lineHeight.tight))] overflow-hidden"
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

        <p class="text-xl mb-8 text-center max-w-2xl mx-auto">
          Free up your time by connecting the systems you depend on, by a
          provider you can count on.
        </p>
        <!-- <div class="flex gap-4 items-center justify-center">
          <Button
            class="font-semibold text-base hover:bg-secondary hover:text-white"
            >Take interactive tour
          </Button>
          <Button class="font-semibold text-base bg-white hover:bg-primary"
            >Talk to us</Button
          >
        </div> -->
      </div>
      <div>
        <TheCard
          class="p-10 rounded-3xl mb-12 max-w-2xl mt-10 text-start bg-black mx-auto"
        >
          <h3 class="text-3xl font-bold mb-2 capitalize">
            Your technology partner for digital solutions.
          </h3>
          <p class="text-sm text-gray-300">
            Connectivo assists SME companies in optimizing, connecting, and
            improving their business processes. We are small enough to see,
            listen, and care about our customers' success, yet big enough to
            engage, push, and deliver software that allows businesses to reach
            their target goals.
          </p>
        </TheCard>
      </div>
    </div>
  </div>
</template>

<script setup>
import { MoveRight } from "lucide-vue-next";
import TheCard from "@/components/common/TheCard.vue";
</script>
<style scoped>
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}
</style>
