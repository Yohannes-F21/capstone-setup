<template>
  <div class="bg-white rounded-md shadow-md w-full h-fit mb-10">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Video</h1>
    </div>
    <div>
      <UForm
        :validate="validate"
        :state="state"
        class="space-y-3 w-full p-5"
        @submit="onSubmit"
      >
        <UFormGroup
          label="Video URL"
          name="url"
          size="xl"
          class="my-4"
          help="For example: https://www.youtube.com/watch?v=49d3Gn41IaA"
        >
          <UInput
            placeholder="Enter your video URL"
            input-class=" rounded-sm  w-full focus:border-indigo"
            variant="outline"
            ui="color:{white:{outline:{focus:ring-indigo-500 dark:focus:ring-indigo-400}}}"
          />
        </UFormGroup>
      </UForm>
    </div>
  </div>
</template>

<script setup></script>
