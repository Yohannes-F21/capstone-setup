<template>
  <div class="bg-white rounded-md shadow-md w-full h-fit mb-10">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Description</h1>
    </div>
    <div>
      <UForm
        :validate="validate"
        :state="state"
        class="space-y-3 w-full p-5"
        @submit="onSubmit"
      >
        <UFormGroup
          label="Property Title"
          name="propertyTitle"
          required="true"
          size="xl"
          class="my-4"
        >
          <UInput
            placeholder="Enter your property title"
            input-class=" rounded-sm  w-full focus:border-indigo"
            variant="outline"
            ui="color:{white:{outline:{focus:ring-indigo-500 dark:focus:ring-indigo-400}}}"
          />
        </UFormGroup>

        <UFormGroup label=" Content" name="content" size="xl" class="my-4">
          <UTextarea size="lg" placeholder="Enter your content" resize />
        </UFormGroup>

        <div class="sm:flex w-full sm:gap-8">
          <UFormGroup
            label=" Type"
            required="true"
            name="type"
            size="xl"
            class="my-4 sm:flex-1"
          >
            <USelect v-model="type" :options="typeOptions" size="xl" />
          </UFormGroup>
          <UFormGroup
            label=" Status"
            required="true"
            name="status"
            size="xl"
            class="my-4 sm:flex-1"
          >
            <USelect v-model="status" :options="statusOptions" />
          </UFormGroup>
          <UFormGroup
            label=" Label"
            required="true"
            name="label"
            size="xl"
            class="my-4 sm:flex-1"
          >
            <USelect v-model="label" :options="labelOptions" />
          </UFormGroup>
        </div>
      </UForm>
    </div>
  </div>
  <div class="bg-white rounded-md shadow-md w-full h-fit">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Price</h1>
    </div>
    <div>
      <UForm
        :validate="validate"
        :state="state"
        class="space-y-3 w-full p-5"
        @submit="onSubmit"
      >
        <div class="sm:flex w-full gap-8">
          <UFormGroup
            label=" Currency"
            name="currency"
            size="xl"
            class="my-4 sm:flex-1"
          >
            <USelect v-model="currency" :options="currencyOptions" size="xl" />
          </UFormGroup>

          <UFormGroup
            label="Sale Price"
            required="true"
            name="salePrice"
            size="xl"
            class="my-4 sm:flex-1"
          >
            <UInput
              placeholder="Enter the price"
              input-class="   w-full focus:border-indigo"
              variant="outline"
            />
          </UFormGroup>
        </div>
      </UForm>
    </div>
  </div>
</template>

<script setup>
const typeOptions = ["none", "house", "apartment", "flat", "villa", "condo"];
const statusOptions = ["none", "house", "apartment", "flat", "villa", "condo"];
const labelOptions = ["none", "house", "apartment", "flat", "villa", "condo"];
const currencyOptions = ["ETB", "USD"];

const type = ref(typeOptions[0]);
const status = ref(statusOptions[0]);
const label = ref(labelOptions[0]);
const currency = ref(currencyOptions[0]);
</script>

<style scoped>
label {
  @apply !font-black;
}
</style>
