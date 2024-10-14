<template>
  <header
    :class="[
      'sticky top-3 flex p-2 items-center gap-4 z-20 md:border container rounded-full backdrop-blur-[20px] backdrop-saturate-[180%] transition-all duration-300',
      isScrolled ? 'bg-[rgb(12_10_9_/_83%)]' : 'bg-transparent',
    ]"
  >
    <div class="container flex items-center justify-between p-0 w-full">
      <div class="flex gap-2">
        <img src="/public/logo.png" class=" ms-4" width="40px" />

        <router-link
          to="/"
          class="flex items-center font-bold whitespace-nowrap uppercase text-lg md:text-xl"
        >
          Connectivo
        </router-link>
        <router-link to="/"> </router-link>
      </div>

      <nav
        class="hidden md:flex flex-1 justify-center gap-6 text-lg font-medium md:gap-5 md:text-sm lg:gap-6"
      >
        <router-link
          v-for="(link, index) in navLinks"
          :key="index"
          :to="link.href"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          {{ link.text }}
        </router-link>
      </nav>
      <div class="flex items-center gap-4">
        <router-link class="hidden md:block" to="/products">
          <Button class="rounded-full h-9 w-full">Saas Products</Button>
        </router-link>
        <Button
          @click="toggleMobileMenu"
          variant="outline"
          size="icon"
          class="md:hidden"
        >
          <Icon
            :icon="
              mobileMenuOpen
                ? 'radix-icons:cross-1'
                : 'radix-icons:hamburger-menu'
            "
            class="h-[1.2rem] w-[1.2rem]"
          />
          <span class="sr-only">Toggle navigation menu</span>
        </Button>
      </div>
    </div>
  </header>
  <Transition name="slide">
    <div
      v-if="mobileMenuOpen"
      class="fixed inset-0 bg-background z-30 md:hidden"
    >
      <div class="flex flex-col h-full p-6">
        <div class="flex justify-between items-center mb-8">
          <div class="flex gap-2">
        <img src="/public/logo.png"   width="40px" />

        <router-link
          to="/"
          class="flex items-center font-bold whitespace-nowrap uppercase text-lg md:text-xl"
        >
          Connectivo
        </router-link>
        <router-link to="/"> </router-link>
      </div>
          <Button @click="toggleMobileMenu" variant="outline" size="icon">
            <Icon icon="radix-icons:cross-1" class="h-[1.2rem] w-[1.2rem]" />
          </Button>
        </div>
        <nav class="flex flex-col gap-6 text-lg font-medium">
          <router-link
            v-for="(link, index) in navLinks"
            :key="index"
            :to="link.href"
            class="text-muted-foreground transition-colors hover:text-foreground"
            @click="closeMobileMenu"
          >
            {{ link.text }}
          </router-link>
        </nav>
        <div class="mt-auto">
          <router-link to="/products">
            <Button class="rounded-full h-9 w-full">Saas Products</Button>
          </router-link>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { useRouter } from "vue-router";
import { Icon } from "@iconify/vue";

const router = useRouter();
const isScrolled = ref(false);
const mobileMenuOpen = ref(false);

const navLinks = ref([
  { text: "Home", href: "/" },
  { text: "Services", href: "/#services" },
  { text: "Our Process", href: "/#process" },
  { text: "Platform Integrations", href: "/#IntegrationsSection" },
  { text: "Contact", href: "#contact" },
]);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value;
  if (mobileMenuOpen.value) {
    document.body.style.overflow = "hidden";
  } else {
    document.body.style.overflow = "";
  }
};

const closeMobileMenu = () => {
  mobileMenuOpen.value = false;
  document.body.style.overflow = "";
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
  router.afterEach(() => {
    closeMobileMenu();
  });
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease;
}

.slide-enter-from,
.slide-leave-to {
  transform: translateX(-100%);
}
</style>
