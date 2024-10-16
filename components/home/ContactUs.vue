<template>
  <section
    id="contact"
    class="bg-gradient-to-b from-[#0D1117] via-[black] to-[#1E2368]"
  >
    <div
      class="flex flex-col md:flex-row items-center container gap-10 py-8 md:pt-[150px]"
    >
      <!-- Left side content -->
      <div class="md:max-w-xl w-full flex flex-col justify-between">
        <h1 class="text-4xl sm:text-5xl md:text-7xl font-bold mb-2">
          Resquest A
          <span class="text-primary">Free Trial</span>
        </h1>
        <p class="text-gray-400">
          Email, call, or complete the form to learn how Connectivo can solve
          your messaging problem.
        </p>
        <div class="flex flex-col my-5 text-sm">
          <div class="flex items-center mb-2 gap-2 text-gray-400">
            <Mail size="16" />
            <a href="mailto:info@connectivo.se"> info@connectivo.se</a>
          </div>
          <div class="flex gap-2 text-gray-400">
            <Phone size="16" />
            <a href="tel:+0106411212">010-641 12 12</a>
          </div>
        </div>
        <div class="grid grid-col-1 md:grid-cols-2">
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
      <!-- Right side form -->
      <div class="w-full">
        <form @submit.prevent="submitForm" class="space-y-6">
          <div class="grid grid-cols-2 gap-6">
            <Input
              v-model="firstName"
              type="text"
              required
              placeholder="First Name"
              class="form-input placeholder:text-white 400placeholder-red-"
            />
            <Input
              v-model="lastName"
              type="text"
              required
              placeholder="Last Name"
              class="form-input"
            />
          </div>
          <div class="grid grid-cols-2 gap-6">
            <Input
              v-model="email"
              type="email"
              required
              placeholder="Email"
              class="form-input"
            />
            <Input
              v-model="phoneNumber"
              type="tel"
              required
              placeholder="Phone Number"
              class="form-input"
            />
          </div>
          <Textarea
            v-model="message"
            required
            placeholder="Type Your Message"
            rows="6"
            class="form-input"
          ></Textarea>
          <div class="flex items-center justify-between">
            <div class="flex items-center">
              <Checkbox class="border-primary" />
              <Label for="terms" class="ml-2 text-sm"
                >I agree to the website terms and conditions</Label
              >
            </div>
            <Button type="submit"> Send </Button>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const phoneNumber = ref("");
const message = ref("");
const agreeToTerms = ref(false);

const submitForm = () => {
  // Handle form submission logic here
  console.log("Form submitted", {
    firstName,
    lastName,
    email,
    phoneNumber,
    message,
    agreeToTerms,
  });
};
</script>
