<template>
  <section id="contact" class="container pt-0 py-[150px]">
    <div class="flex flex-col-reverse md:flex-row gap-20 relative">
      <div class="flex-1 z-10">
        <h1
          class="text-4xl mb-2 md:text-6xl font-extrabold md:mb-3 leading-tight"
        >
          Contact Us
        </h1>
        <p class="text-gray-400 md:text-lg">
          Email, call, or complete the form to learn how Connectivo can solve
          your messaging problem.
        </p>
        <div class="flex flex-col mt-5 md:mt-10 text-sm">
          <div class="flex items-center mb-2 gap-2 text-gray-400">
            <Mail size="16" />
            <a href="mailto:info@connectivo.se"> info@connectivo.se</a>
          </div>
          <div class="flex gap-2 text-gray-400">
            <Phone size="16" />
            <a href="tel:+0106411212">010-641 12 12</a>
          </div>
        </div>
        <div class="mt-5 md:mt-10 grid grid-col-1 md:grid-cols-2">
          <div class="mb-4">
            <h3 class="font-bold mb-1">Customer Support</h3>
            <p class="text-gray-400 text-xs">
              Our support team is available around the clock to address any
              concerns or queries you may have.
            </p>
          </div>

          <div class="mb-4">
            <h3 class="font-bold mb-1">Feedback and Suggestions</h3>
            <p class="text-gray-400 text-xs">
              We value your feedback and are continuously working to improve
              Connectivo. Your input is crucial in shaping the future of
              Connectivo.
            </p>
          </div>

          <div>
            <h3 class="font-bold mb-1">Media Inquiries</h3>
            <p class="text-gray-400 text-xs">
              For media-related questions or press inquiries, please contact us
              at
              <a href="mailto:info@connectivo.se" class="text-primary">
                info@connectivo.se</a
              >
            </p>
          </div>
        </div>
      </div>

      <div class="flex-1 z-10 mt-20 md:mt-0">
        <div class="md:border-l md:ps-20">
          <h1
            class="text-4xl mb-2 md:text-6xl font-extrabold md:mb-3 leading-tight"
          >
            Get in Touch
          </h1>
          <p class="text-gray-400 md:text-lg">You can reach us anytime.</p>

          <form @submit.prevent="submitForm" class="space-y-4 mt-10">
            <div class="flex gap-4">
              <div class="w-full">
                <Input
                  type="text"
                  placeholder="First name"
                  v-model="firstName"
                  id="name"
                  required
                  class="h-12 w-full py-4 px-6 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
                />
              </div>
              <div class="w-full">
                <Input
                  type="text"
                  placeholder="Last name"
                  v-model="lastName"
                  id="name"
                  required
                  class="h-12 w-full py-4 px-6 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
                />
              </div>
            </div>
            <div>
              <Input
                type="email"
                placeholder="Email"
                id="email"
                v-model="email"
                required
                class="h-12 w-full py-4 px-6 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
              />
            </div>
            <Textarea
              v-model="message"
              placeholder="How can we help?"
              rows="5"
              class="w-full p-4 border rounded-2xl bg-background"
              required
            ></Textarea>
            <Button type="submit" class="w-full rounded-full text-xl h-12">
              Submit
            </Button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
import { Send, Mail, Phone } from "lucide-vue-next";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const phoneNumber = ref("");
const message = ref("");

const submitForm = () => {
  // Handle form submission logic here
  console.log("Form submitted:", {
    firstName: firstName.value,
    lastName: lastName.value,
    email: email.value,
    phoneNumber: phoneNumber.value,
    message: message.value,
  });
};
</script>
