<template>
  <div
    class="message-input flex w-full border items-center shadow-sm rounded-lg border-gray-300 py-1 px-2 focus-within:border-green-700"
  >
    <input
      type="text"
      class="flex-1 outline-none border-0 bg-white focus:ring-0"
      v-model="model"
    />
    <button
      class="inline-flex items-center justify-center shadow-sm bg-green-700 text-white hover:bg-green-700/90 border-green-700 h-[32px] px-[15px] py-[8px] text-sm rounded-[4px]"
      @click="onCreate"
    >
      <Icon icon="radix-icons:paper-plane"></Icon>
      发送
    </button>
  </div>
</template>

<script lang="ts" setup>
import { Icon } from "@iconify/vue";

const emit = defineEmits<{
  create: [value: string];
}>();
const model = defineModel<string>();
const onCreate = () => {
  if (model.value.trim() !== "") {
    emit("create", model.value);
  }
};
</script>
