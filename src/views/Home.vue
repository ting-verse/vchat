<template>
  <div class="w-[80%] mx-auto h-full">
    <div class="flex items-center h-[85%]">
      {{ selectedModel }}
      <ProviderSelect :items="providers" v-model="selectedModel" />
    </div>
    <div class="flex items-center h-[15%]">
      <MessageInput />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { ProviderProps } from "../types";
import ProviderSelect from "../components/ProviderSelect.vue";
import MessageInput from "../components/MessageInput.vue";
const selectedModel = ref("");

const providers: ProviderProps[] = [
  {
    id: 1,
    name: "文心一言",
    desc: "文心一言 百度出品的大模型",
    models: ["ERNIE-4.0-8K", "ERNIE-3.5-8K", "ERNIE-Speed-8K"],
    avatar: "https://picsum.photos/id/180/200/200",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
  },
  {
    id: 2,
    name: "通义千问",
    desc: "通义千问",
    models: ["qwen-turbo", "qwen-plus", "qwen-max"],
    avatar: "https://picsum.photos/id/180/200/200",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
  },
];
console.log('👋 This message is being logged by "App.vue", included via Vite');
</script>
