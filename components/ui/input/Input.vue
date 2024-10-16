<template>
  <div>
    <Label v-if="label" :for="name" class="block text-sm font-medium mb-1">{{
      label
    }}</Label>
    <input
      v-bind="$attrs"
      :id="name"
      v-model="modelValue"
      :class="inputClass"
      @blur="handleBlur"
    />
    <h6 v-if="error" class="text-red-500 text-sm mt-1">{{ error }}</h6>
  </div>
</template>
<script setup>
import { useVModel } from "@vueuse/core";
import { cn } from "@/lib/utils";
import { computed } from "vue";

const props = defineProps({
  defaultValue: { type: [String, Number], required: false },
  modelValue: { type: [String, Number], required: false },
  name: { type: String },
  label: { type: String },
  error: { type: String, default: "" },
  validate: { type: Function },
  class: { type: [String, Object, Array], default: "" },
});

const emits = defineEmits(["update:modelValue"]);

const modelValue = useVModel(props, "modelValue", emits, {
  passive: true,
  defaultValue: props.defaultValue,
});

const handleBlur = () => {
  if (props.validate) {
    props.validate(props.name);
  }
};

const inputClass = computed(() => {
  return cn(
    "flex h-10 w-full rounded-[6px] bg-black   border-white p-6 text-sm ring-offset-background file:border-0 file:bg-transparent file:text-sm file:font-medium placeholder:text-white  focus-visible:outline-2 focus-visible:ring-none focus-visible:ring-ring focus-visible:ring-offset-none disabled:cursor-not-allowed disabled:opacity-50",
    { "border-red-500": props.error },
    props.class
  );
});
</script>
