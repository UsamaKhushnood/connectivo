<template>
  <div
    class="text-card-foreground min-h-[calc(100vh-180px)] flex items-center justify-center"
  >
    <div
      class="w-full mx-auto text-center bg-[url('/block.png')] overflow-hidden md:py-[200px] md:px-20 relative"
    >
      <div
        class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]"
      ></div>
      <div class="z-2 relative">
        <div class="container md:grid md:grid-cols-2 md:pt-20 pb-2">
          <div class="text-start">
            <h1
              class="text-4xl md:text-6xl text-center md:text-start font-extrabold md:mb-6 mb-2 leading-tight"
            >
              Connect the dots.
            </h1>
            <p
              class="text-center md:text-start text-lg md:text-2xl text-gray-400 mb-4 md:mb-10 max-w-3xl auto"
            >
              Free up your time by connecting the systems you depend on, by a
              provider you can count on.
            </p>
            <div class="md:space-x-4 flex flex-col items-center md:block">
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
          </div>
          <div class=""></div>
          <div class=""></div>
          <div
            class="mt-20 max-w-xl md:border rounded-2xl text-start bg-background md:p-6 md:outline outline-2 outline-orange-800 outline-offset-[6px] md:-mt-[75px] ms-auto"
          >
            <h1 class="text-2xl font-bold flex gap-4 md:text-start">
              <MessageCircleMore class="mt-2 hidden md:block" />
              Your technology partner for digital solutions.
            </h1>
            <p class="mt-2 mx-auto text-gray-500 md:pl-9 md:text-start">
              Connectivo assists SME companies in optimizing, connecting, and
              improving their business processes. We are small enough to see,
              listen and care about our customers success, yet big enough to
              engage, push and deliver software which allows for businesses to
              reach their target goals.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ChevronRight, MessageCircleMore } from "lucide-vue-next";
</script>
