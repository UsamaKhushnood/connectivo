<template>
  <header
    class="sticky top-2 flex h-16 items-center gap-4 z-20 border container rounded-full mt-2 px-4 bg-[rgb(12_10_9_/_83%)] backdrop-blur-[20px] backdrop-saturate-[180%]"
  >
    <div class="container flex items-center justify-between p-0">
      <router-link
        to="/"
        class="flex items-center gap-2 font-bold ms-4 whitespace-nowrap uppercase"
      >
        Connectivo
      </router-link>
      <nav
        class="flex-1 flex justify-center hidden gap-6 text-lg font-medium md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
      >
        <a
          v-for="(link, index) in navLinks"
          :key="index"
          :href="link.href"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          {{ link.text }}
        </a>
      </nav>
      <Sheet>
        <SheetTrigger as-child>
          <Button variant="outline" size="icon" class="shrink-0 md:hidden">
            <Icon
              icon="radix-icons:hamburger-menu"
              class="h-[1.2rem] w-[1.2rem]"
            />
            <span class="sr-only">Toggle navigation menu</span>
          </Button>
        </SheetTrigger>
        <SheetContent class="rounded-e-xl" side="left">
          <nav class="grid gap-3 text-lg font-medium">
            <router-link
              to="/"
              class="text-lg font-bold md:text-base whitespace-nowrap mb-10"
            >
              Connectivo
            </router-link>
            <a
              v-for="(link, index) in navLinks"
              :key="index"
              :href="link.href"
              class="text-muted-foreground transition-colors hover:text-foreground"
            >
              {{ link.text }}
            </a>
          </nav>
        </SheetContent>
      </Sheet>
      <div class="ms-auto">
        <Button class="rounded-full">Saas Products</Button>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { cn } from "@/lib/utils";
import { Icon } from "@iconify/vue";

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});

const navLinks = ref([
  { text: "Home", href: "/#" },
  { text: "Services", href: "/#PlatformIntegrations" },
  { text: "Platform Integrations", href: "/#IntegrationsSection" },
  { text: "Our Process", href: "/#get-started" },
  { text: "Our Customers", href: "/#pricing" },
  { text: "Contact", href: "/#contact" },
]);
</script>
