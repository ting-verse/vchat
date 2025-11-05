Vue3.5+Electron+大模型 跨平台AI桌面聊天应用实战 / vchat 温馨提示：Git用户名 /
Username: ting-verse Git密码 / Password: 为慕课网登录密码 重置密码 App.vue 3.4
KB 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29
30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56
57 58 59 60 61 62 63 64 65 66 67 68 69
<template>
  <div class="flex items-center justify-between h-screen">
    <div class="w-[300px] bg-gray-200 h-full border-r border-gray-300">
      <div class="h-[90%] overflow-y-auto">
        <ConversationList :items="items" />
      </div>
      <div class="h-[10%] grid grid-cols-2 gap-2 p-2">
        <button
          class="shadow-sm inline-flex items-center justify-center bg-green-700 text-white hover:bg-green-700/90 border border-green-700 h-[32px] py-[8px] px-[15px] text-sm rounded-[4px]"
        >
          <Icon icon="radix-icons:chat-bubble" class="mr-2"></Icon>
          新建聊天
        </button>
        <button
          class="shadow-sm inline-flex items-center justify-center bg-green-50 text-green-700 hover:bg-green-700 border border-green-700 hover:text-white h-[32px] py-[8px] px-[15px] text-sm rounded-[4px]"
        >
          <Icon icon="radix-icons:gear" class="mr-2"></Icon>
          应用设置
        </button>
      </div>
    </div>
    <div class="h-full flex-1">
      <ProviderSelect :items="providers" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { Icon } from "@iconify/vue";
import { ConversationProps, ProviderProps } from "./types";
import ConversationList from "./components/ConversationList.vue";
import ProviderSelect from "./components/ProviderSelect.vue";
const items: ConversationProps[] = [
  {
    id: 1,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用1",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 2,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 3,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 4,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用, 你的说法很请正确，理解的很不错",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 5,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用1",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 6,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 7,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
  {
    id: 8,
    selectedModel: "GPT-3.5-Turbo",
    title: "什么是光合作用, 你的说法很请正确，理解的很不错",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
    providerId: 1,
  },
];
const providers: ProviderProps[] = [
  {
    id: 1,
    name: "文心一言",
    desc: "文心一言 百度出品的大模型",
    models: ["ERNIE-4.0-8K", "ERNIE-3.5-8K", "ERNIE-Speed-8K"],
    avatar:
      "https://qph.cf2.poecdn.net/main-thumb-pb-3004-50-jougqzjtwfqfyqprxbdwofvnwattmtrg.jpeg",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
  },
  {
    id: 2,
    name: "通义千问",
    desc: "通义千问",
    // https://help.aliyun.com/zh/dashscope/developer-reference/api-details?spm=a2c4g.11186623.0.0.5bf41507xgULX5#b148acc634pfc
    models: ["qwen-turbo", "qwen-plus", "qwen-max"],
    avatar:
      "https://qph.cf2.poecdn.net/main-thumb-pb-3004-50-jougqzjtwfqfyqprxbdwofvnwattmtrg.jpeg",
    createdAt: "2024-07-03",
    updatedAt: "2024-07-03",
  },
];
console.log('👋 This message is being logged by "App.vue", included via Vite');
</script>
Copyright © 2018 imooc.com All Rights Reserved | 京ICP备 12003892号-11 简体中文
