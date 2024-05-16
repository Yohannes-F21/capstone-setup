<template>
  <div>
    <!-- <Header></Header> -->
    <div class="bg-[#F7F8F9] flex">
      <ListingSideBar class="hidden sm:block h-screen"></ListingSideBar>
      <div class="flex-1 overflow-y-auto max-h-screen">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style></style>
