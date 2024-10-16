<script setup lang="ts">
import type { HTMLAttributes } from "vue";
import { useVModel } from "@vueuse/core";
import { cn } from "@/lib/utils";

const props = defineProps<{
  class?: HTMLAttributes["class"];
  defaultValue?: string | number;
  modelValue?: string | number;
}>();

const emits = defineEmits<{
  (e: "update:modelValue", payload: string | number): void;
}>();

const modelValue = useVModel(props, "modelValue", emits, {
  passive: true,
  defaultValue: props.defaultValue,
});
</script>

<template>
  <textarea
    v-model="modelValue"
    :class="
      cn(
        'flex min-h-20 w-full  bg-[#090B1F] opacity-20 border border-white rounded-[6px]  p-6 text-sm ring-offset-background-none placeholder:text-muted-foreground focus-visible:outline-2 focus-visible:ring-none focus-visible:ring-ring focus-visible:ring-offset-none disabled:cursor-not-allowed disabled:opacity-50',
        props.class
      )
    "
  />
</template>
