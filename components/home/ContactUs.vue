<template>
  <div id="contact" class="container mb-20">
    <div
      class="bg-gradient-to-br from-green-900 to-black rounded-2xl overflow-hidden backdrop-blur-sm"
    >
      <div class="flex p-20">
        <!-- Left side with title and description -->
        <div class="w-2/5">
          <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold">
            Contact
            <span class="text-primary">Us </span>
          </h1>
          <p class="text-gray-300 mt-4 pr-10">
            Email, call, or complete the form to learn how Connectivo can solve
            your messaging problem.
          </p>
          <div class="mt-auto flex items-center gap-2 pt-20">
            <img src="/public/logo.png" alt="GROW logo" class="h-8" />
            <div class="text-4xl font-bold">Connectivo</div>
          </div>
        </div>

        <!-- Right side with form -->
        <div class="w-3/5">
          <form @submit.prevent="submitForm">
            <div class="grid grid-cols-2 gap-4 mb-4">
              <input
                v-model="firstName"
                type="text"
                placeholder="First Name"
                class="input-field"
              />
              <input
                v-model="lastName"
                type="text"
                placeholder="Last Name"
                class="input-field"
              />
            </div>
            <div class="grid grid-cols-2 gap-4 mb-4">
              <input
                v-model="email"
                type="email"
                placeholder="Email"
                class="input-field"
              />
              <input
                v-model="phoneNumber"
                type="tel"
                placeholder="Phone Number"
                class="input-field"
              />
            </div>
            <textarea
              v-model="message"
              placeholder="Type  Your Message"
              rows="4"
              class="input-field mb-4"
            ></textarea>
            <div class="flex items-center justify-between">
              <div class="flex items-center mb-6">
                <Checkbox
                  v-model="agreeTerms"
                  type="checkbox"
                  id="terms"
                  class="mr-2"
                />
                <Label for="terms" class="text-sm text-gray-400"
                  >I agree to the website terms and conditions</Label
                >
              </div>

              <Button
                type="submit"
                class="py-3 px-20 bg-gradient-to-br from-green-300 to-green-900 rounded-full text-black font-semibold hover:from-green-500 hover:to-green-600 transition duration-300"
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

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const phoneNumber = ref("");
const message = ref("");
const agreeTerms = ref(false);

const submitForm = () => {
  // Handle form submission
  console.log("Form submitted", {
    firstName,
    lastName,
    email,
    phoneNumber,
    message,
    agreeTerms,
  });
};
</script>

<style scoped>
.input-field {
  @apply w-full p-3 rounded-2xl bg-green-900 bg-opacity-30 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-green-500;
}
</style>
