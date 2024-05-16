<template>
  <div
    class="sticky mt-auto bottom-0 inset-x-0 shadow-md p-4 bg-[#fff] flex flex-row flex-wrap justify-between items-center tracking-[normal] leading-[normal] text-left text-base text-[#839EA8]"
  >
    <UButton
      color="indigo"
      variant="outline"
      class="hover:bg-indigo-500 hover:text-white"
    >
      Cancel
    </UButton>
    <UButton color="indigo">
      Next
      <template #trailing>
        <UIcon name="i-heroicons-arrow-right-20-solid" class="w-5 h-5" />
      </template>
    </UButton>
  </div>
</template>

<script lang="ts" setup></script>
