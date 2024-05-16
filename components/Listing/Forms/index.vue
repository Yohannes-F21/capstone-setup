<template>
  <div class="w-full min-h-screen">
    <ListingFormsHeader></ListingFormsHeader>
    <section class="sm:w-[70%] sm:ml-8 my-6 mx-5">
      <component
        :is="steps[currentStep].component"
        :step="steps[currentStep]"
        @next="nextStep"
        @previous="previousStep"
      ></component>
    </section>
    <div
      class="sticky mt-auto bottom-0 inset-x-0 shadow-md p-4 bg-[#fff] flex flex-row flex-wrap justify-between items-center tracking-[normal] leading-[normal] text-left text-base text-[#839EA8]"
    >
      <UButton
        color="indigo"
        variant="outline"
        class="hover:bg-indigo-500 hover:text-white"
        @click="previousStep"
      >
        {{ isFirstStep }}
      </UButton>
      <UButton color="indigo" @click="nextStep">
        {{ isLastStep }}
        <template #trailing>
          <UIcon name="i-heroicons-arrow-right-20-solid" class="w-5 h-5" />
        </template>
      </UButton>
    </div>
  </div>
</template>

<script setup>
const router = useRouter();
const route = useRoute();
const currentStep = ref(0);

// console.log(route.params.value);

const steps = [
  {
    name: "basicInfo",
    label: "Basic Info",
    component: resolveComponent("ListingFormsBasicInfoForm"),
  },
  {
    name: "media",
    label: "Media",
    component: resolveComponent("ListingFormsMediaForm"),
  },
  {
    name: "details",
    label: "Details",
    component: resolveComponent("ListingFormsDetailsForm"),
  },
  {
    name: "location",
    label: "Location",
    component: resolveComponent("ListingFormsLocationForm"),
  },
];

const nextStep = () => {
  //validate form
  currentStep.value++;
};

const previousStep = () => {
  // console.log(isFirstStep.value);
  if (isFirstStep.value === "Cancel") {
    return router.back();
  }
  currentStep.value--;
};

const isLastStep = computed(() => {
  if (currentStep.value === steps.length - 1) {
    return "Submit";
  } else {
    return "Next";
  }
});

const isFirstStep = computed(() => {
  if (currentStep.value === 0) {
    return "Cancel";
  } else {
    return "Previous";
  }
});
</script>

<style></style>
