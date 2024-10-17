<template>
  <div
    class="min-h-[800px] h-screen flex flex-col items-center justify-center text-white p-8 bg-gradient-to-br from-blue-950 via-black to-blue-400  -mt-[55px]"
  >
    <div class="text-start">
      <div class="flex gap-3 items-center font-extrabold text-4xl md:text-8xl">
        <h1 class="whitespace-pre">Connect the</h1>
        <div
          class="text-primary inline-flex flex-col min-h-[calc(theme(fontSize.8xl)*theme(lineHeight.tight))] md:h-[calc(theme(fontSize.4xl)*theme(lineHeight.tight))] overflow-hidden"
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

    <p class="text-xl mb-8 text-center max-w-2xl">
      Free up your time by connecting the systems you depend on, by a provider
      you can count on.
    </p>
    <TheCard class="p-6 rounded-3xl mb-12 max-w-3xl mt-4">
      <h3 class="text-3xl font-semibold mb-2 capitalize">
        Your technology partner for digital solutions.
      </h3>
      <p class="text-sm text-gray-300">
        Connectivo assists SME companies in optimizing, connecting, and
        improving their business processes. We are small enough to see, listen,
        and care about our customers' success, yet big enough to engage, push,
        and deliver software that allows businesses to reach their target goals.
      </p>
    </TheCard>
  </div>
</template>

<script setup>
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
