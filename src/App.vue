<template>
  <div class="flex items-center justify-between h-screen">
    <div class="bg-gray-300 text-gray-700 w-[10rem] h-full hover:bg-yellow-300">
      sidebar
    </div>
    <div class="bg-green-300 text-blue-700 h-full flex-1">
      content
      <input
        type="text"
        placeholder="Search for anything"
        class="placeholder:text-blue-300"
      />
    </div>
  </div>
</template>

<script setup></script>
