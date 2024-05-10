<template>
  <div
    class="absolute top-[288.3px] left-[1290.2px] shadow-[3px_3px_15px_rgba(149,_149,_149,_0.05)] w-[397.2px] h-[213.3px] z-[1] text-left text-base text-slate-gray-pg-color font-inter"
    :style="bGStyle"
  >
    <img
      class="absolute top-[181.2px] left-[31.7px] w-[35px] h-[32.2px]"
      alt=""
      src="/vector-2-3.svg"
    />
    <div
      class="absolute top-[0px] left-[0px] rounded-mini bg-main-color-white w-[397.2px] h-[191.9px] z-[1]"
    >
      <div
        class="absolute top-[0px] left-[0px] rounded-mini bg-main-color-white w-full h-full hidden"
      />
      <div
        class="absolute top-[40.7px] left-[39.4px] leading-[26px] inline-block w-[310.8px] h-[104px] z-[2]"
        :style="iHaveInsuranceContainerStyle"
      >
        <p class="m-0">{{ iHaveInsuranceAndStillGoT }}</p>
        <p class="m-0">{{ clinicTheCostIsInLineWith }}</p>
        <p class="m-0">{{ toDoAndIDontNeedToMakeAn }}</p>
        <p class="m-0">{{ appointment }}</p>
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  iHaveInsuranceAndStillGoT: { type: String },
  clinicTheCostIsInLineWith: { type: String },
  toDoAndIDontNeedToMakeAn: { type: String },
  appointment: { type: String },
  propLeft: { type: [Object, Array, String, Number, Boolean] },
  propWidth: { type: [Object, Array, String, Number, Boolean] },
});
</script>
