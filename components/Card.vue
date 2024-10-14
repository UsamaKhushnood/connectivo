<template>
  <div class="relative overflow-hidden">
    <div
      :style="{ width }"
      class="h-full rounded-2xl border border-transparent p-6 gradient-background"
    >
      <div class="space-y-2">
        <h2 class="text-2xl font-bold text-slate-200">{{ title }}</h2>
        <p class="text-sm font-medium text-slate-500">{{ description }}</p>
        <div v-if="hasActions" class="flex space-x-4 mt-4">
          <slot name="actions"></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GradientCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    hasActions: {
      type: Boolean,
      default: false,
    },
    width: {
      type: String,
      default: "100%", // Default to full width
    },
  },
};
</script>

<style scoped>
@property --border-angle {
  syntax: "<angle>";
  inherits: false;
  initial-value: 0deg;
}

.gradient-background {
  background: linear-gradient(
        45deg,
        #172033,
        theme("colors.slate.800") 50%,
        #172033
      )
      padding-box,
    conic-gradient(
        from var(--border-angle),
        theme("colors.slate.600") 0%,
        theme("colors.indigo.500") 20%,
        theme("colors.indigo.300") 40%,
        theme("colors.indigo.500") 60%,
        theme("colors.slate.600") 80%
      )
      border-box;
  animation: border-rotate 6s linear infinite;
}

@keyframes border-rotate {
  from {
    --border-angle: 0deg;
  }
  to {
    --border-angle: 360deg;
  }
}
</style>
