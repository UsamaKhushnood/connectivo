<template>
  <div
    class="text-white p-8 bg-[url('/public/bg-green.png')] bg-contain bg-no-repeat bg-right-top bg-black -mt-[55px]"
  >
    <div class="container">
      <div class="mx-auto w-fit text-center mb-[120px] pt-[200px]">
        <div class="text-start">
          <h1 class="text-6xl font-extrabold max-w-5xl text-center">
            Standard solutions for common problems.
          </h1>
        </div>

        <p class="text-xl mb-8 text-center max-w-2xl mx-auto mt-6">
          SaaS services built to empower companies and accelerate their digital
          journey.
        </p>
      </div>
      <div>
        <div
          class="text-black shadow-lg p-10 rounded-xl mb-12 mt-10 max-w-6xl text-start bg-gradient-to-r from-green-200 via-teal-400 to-cyan-600 mx-auto"
        >
          <h3 class="text-3xl font-extrabold mb-2 capitalize">
            Entrepeneurship is tough. We are here to make it easier.
          </h3>
          <div class="text-sm font-medium space-y-3 mt-4">
            <p>
              Connectivo was founded 2013 and spent the first 4 years of trade
              in e-commerce, selling in a variety of countries and marketplaces.
              We found early on a variety of friction points and time consuming
              manual steps which prevented us from realizing the target goals.
              With every problem, a bigger solution can be found. After some
              years of frustration, we decided to drop what we were doing and
              get to the root of the problem.
            </p>
            <p>
              With a background in IT, accounting, e-commerce, finance and
              business development we merged all experiences together and
              started designing and coding software solutions to help push
              entrepeneurs forward. Today Connectivo provides standardized apps
              and platforms which solve common problems within a variety of
              industries.
            </p>
            <p>
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
  <OurProducts />
</template>
<script>
import OurProducts from "~/components/products/OurProducts.vue";
export default {
  components: { OurProducts },
};
</script>
