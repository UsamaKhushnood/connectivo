<template>
  <div id="contact" class="container mx-auto px-4 my-20">
    <div
      class="bg-gradient-to-r from-pink-500 via-red-500 to-orange-500 rounded-2xl overflow-hidden backdrop-blur-sm"
    >
      <div class="flex flex-col lg:flex-row p-6 sm:p-10 lg:p-20">
        <!-- Left side with title and description -->
        <div class="w-full lg:w-2/5 mb-8 lg:mb-0">
          <h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-extrabold">
            Contact Us
          </h1>
          <p class="text-white mt-4 lg:pr-10">
            Email, call, or complete the form to learn how Connectivo can solve
            your messaging problem.
          </p>
          <div class="mt-8 lg:mt-auto md:flex items-center gap-2 pt-8 lg:pt-20 hidden">
            <img src="/public/logo.png" alt="GROW logo" class="h-6 sm:h-8" />
            <div class="text-2xl sm:text-3xl lg:text-4xl font-bold">Connectivo</div>
          </div>
        </div>

        <!-- Right side with form -->
        <div class="w-full lg:w-3/5">
          <form @submit.prevent="submitForm">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-4">
              <Input
                v-model="firstName"
                type="text"
                placeholder="First Name"
              />
              <Input
                v-model="lastName"
                type="text"
                placeholder="Last Name"
              />
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-4">
              <Input
                v-model="email"
                type="email"
                placeholder="Email"
              />
              <Input
                v-model="phoneNumber"
                type="tel"
                placeholder="Phone Number"
              />
            </div>
            <Textarea
              v-model="message"
              placeholder="Type Your Message"
              rows="4"
              class="bg-black text-white placeholder-gray-400 mb-4"
            />
            <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between">
              <div class="flex items-start sm:items-center mb-4 sm:mb-0">
                <Checkbox
                  v-model="agreeTerms"
                  id="terms"
                  class="mr-2 border-black"
                />
                <Label for="terms" class="text-sm text-white"
                  >I agree to the website terms and conditions</Label
                >
              </div>

              <Button
                type="submit"
                class="w-full sm:w-auto py-3 px-8 sm:px-20 rounded-full text-white font-semibold transition duration-300 bg-black hover:bg-gray-800"
              >
                Send
              </Button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Checkbox } from "@/components/ui/checkbox";
import { Label } from "@/components/ui/label";
import { Button } from "@/components/ui/button";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const phoneNumber = ref("");
const message = ref("");
const agreeTerms = ref(false);

const submitForm = () => {
  // Handle form submission
  console.log("Form submitted", {
    firstName: firstName.value,
    lastName: lastName.value,
    email: email.value,
    phoneNumber: phoneNumber.value,
    message: message.value,
    agreeTerms: agreeTerms.value,
  });
};
</script>