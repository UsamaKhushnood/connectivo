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
              class="text-2xl md:text-6xl font-extrabold md:mb-6 mb-2 leading-tight"
            >
              Standard solutions for common problems.
            </h1>
            <p
              class="text-lg md:text-2xl text-gray-400 mb-4 md:mb-10 max-w-3xl auto"
            >
              SaaS services built to empower companies and accelerate their
              digital journey.
            </p>
            <div class="md:space-x-4">
              <router-link :to="{ path: '/', hash: '#contact' }">
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
            class="border rounded-2xl text-start bg-background p-6 outline outline-2 outline-orange-800 outline-offset-[6px] mt-10 md:-mt-[150px] md:ml-10 ms-auto"
          >
            <h1 class="text-2xl font-bold flex gap-4">
              <MessageCircleMore class="mt-2" />
              Entrepeneurship is tough. We are here to make it easier.
            </h1>
            <p class="mt-2 mx-auto text-gray-500 pl-9">
              Connectivo was founded 2013 and spent the first 4 years of trade
              in e-commerce, selling in a variety of countries and marketplaces.
              We found early on a variety of friction points and time consuming
              manual steps which prevented us from realizing the target goals.
              With every problem, a bigger solution can be found. After some
              years of frustration, we decided to drop what we were doing and
              get to the root of the problem.
              <br />
              With a background in IT, accounting, e-commerce, finance and
              business development we merged all experiences together and
              started designing and coding software solutions to help push
              entrepeneurs forward. Today Connectivo provides standardized apps
              and platforms which solve common problems within a variety of
              industries.
              <br />
              The company is 100% founder-owned, profitable and fully
              bootstrapped.This allows for us to continously put our clients
              needs above all without compromising on quality, mission or
              vision.
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
