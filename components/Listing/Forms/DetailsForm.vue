<template>
  <div class="bg-white rounded-md shadow-md w-full h-fit mb-20">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Detail</h1>
    </div>
    <div>
      <UForm
        :validate="validate"
        :state="state"
        class="space-y-3 w-full p-5"
        @submit="onSubmit"
      >
        <div class="w-full sm:grid sm:grid-cols-2 sm:gap-x-10">
          <UFormGroup
            label="Bed Rooms"
            name="bedRooms"
            size="xl"
            class="my-4"
            hint="only digits"
          >
            <UInput
              placeholder="Enter Number of Bed Rooms "
              input-class=" rounded-md  w-full "
              variant="outline"
              type="number"
            />
          </UFormGroup>

          <UFormGroup
            label="Rooms"
            name="rooms"
            size="xl"
            class="my-4"
            hint="only digits"
          >
            <UInput
              placeholder="Enter Number of Rooms "
              input-class=" rounded-md  w-full "
              variant="outline"
              type="number"
            />
          </UFormGroup>
          <UFormGroup
            label="Bath Rooms"
            name="bathRooms"
            size="xl"
            class="my-4"
            hint="only digits"
          >
            <UInput
              placeholder="Enter Number of Bath Rooms "
              input-class=" rounded-md  w-full "
              variant="outline"
              type="number"
            />
          </UFormGroup>
          <UFormGroup
            label="Area Size"
            name="areaSize"
            size="xl"
            class="my-4"
            hint="only digits"
          >
            <UInput
              placeholder="Enter Number of Area Size "
              input-class=" rounded-md  w-full "
              variant="outline"
              type="number"
            />
          </UFormGroup>
          <UFormGroup
            label="Year Built"
            name="yearBuilt"
            size="xl"
            class="my-4"
            hint="only digits"
          >
            <UInput
              placeholder="Enter Number of Year Built "
              input-class=" rounded-md  w-full "
              variant="outline"
              type="number"
            />
          </UFormGroup>
        </div>
      </UForm>
    </div>
  </div>
</template>

<script setup></script>
