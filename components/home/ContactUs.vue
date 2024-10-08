<template>
  <section id="contact" class="container my-20">
    <div
      class="flex flex-col md:flex-row gap-8 relative bg-[url('/block.png')]"
    >
      <div
        class="absolute inset-0 -mx-[22px] flex-none overflow-hidden z-1 bg-[radial-gradient(50%_50%_at_50%_50%,rgba(14,15,17,0)_0%,rgb(12_10_9)_100%)]"
      ></div>
      <div class="flex-1 z-10">
        <h1
          class="text-2xl md:text-6xl font-extrabold md:mb-6 mb-2 leading-tight"
        >
          Contact Us
        </h1>
        <p class="mb-4">
          Email, call, or complete the form to learn how Connectivo can solve
          your messaging problem.
        </p>
        <div class="font-bold flex flex-col mb-4">
          <div class="flex items-center mb-2 gap-2">
            <Mail class="text-primary" size="20" />
            <a
              href="mailto:info@connectivo.se"
              class="font-size-sm-12 font-size-md-18 text-decoration-none"
            >
              info@connectivo.se</a
            >
          </div>
          <div class="flex gap-2">
            <Phone class="text-primary" size="20" />
            <a href="tel:+0106411212">010-641 12 12</a>
          </div>
        </div>
        <div class="mb-4">
          <h3 class="font-semibold mb-2">Customer Support</h3>
          <p>
            Our support team is available around the clock to address any
            concerns or queries you may have.
          </p>
        </div>

        <div class="mb-4">
          <h3 class="font-semibold mb-2">Feedback and Suggestions</h3>
          <p>
            We value your feedback and are continuously working to improve
            Connectivo. Your input is crucial in shaping the future of
            Connectivo.
          </p>
        </div>

        <div>
          <h3 class="font-semibold mb-2">Media Inquiries</h3>
          <p>
            For media-related questions or press inquiries, please contact us at
            <span class="text-primary"> info@connectivo.se </span>
          </p>
        </div>
      </div>

      <div class="flex-1 z-10">
        <div class="border p-6 rounded-lg shadow-md bg-background">
          <h2 class="text-4xl font-extrabold mb-4">Get in Touch</h2>
          <p class="mb-4">You can reach us anytime</p>

          <form @submit.prevent="submitForm" class="space-y-4">
            <div class="flex gap-4">
              <div>
                <label for="name" class="text-sm font-medium">
                  First Name
                </label>
                <Input
                  type="text"
                  v-model="firstName"
                  id="name"
                  required
                  class="mt-1 w-full p-4 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
                />
              </div>
              <div>
                <label for="name" class="text-sm font-medium">
                  Last Name
                </label>
                <Input
                  type="text"
                  v-model="lastName"
                  id="name"
                  required
                  class="mt-1 w-full p-4 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
                />
              </div>
            </div>
            <div>
              <label for="email" class="text-sm font-medium">Email</label>
              <Input
                type="email"
                id="email"
                v-model="email"
                required
                class="mt-1 w-full p-4 border rounded-full focus:outline-none focus:ring-0 focus:border-transparent"
              />
            </div>
            <textarea
              v-model="message"
              placeholder="How can we help?"
              class="w-full p-4 border rounded-2xl h-32 bg-background"
              required
            ></textarea>
            <Button type="submit" class="w-full rounded-full gap-2">
              Submit <Send size="20" />
            </Button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
import { ref } from "vue";
import { Input } from "@/components/ui/input";
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
