<template>
  <div class="bg-white rounded-md shadow-md w-full h-fit mb-10">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Location</h1>
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
            label="Adress"
            required="true"
            name="address"
            size="xl"
            class="my-4"
          >
            <UInput
              placeholder="Enter Your Property Address "
              input-class=" rounded-md  w-full "
              variant="outline"
            />
          </UFormGroup>

          <UFormGroup label="City" name="city" size="xl" class="my-4">
            <USelect v-model="city" :options="cities" />
          </UFormGroup>
          <UFormGroup
            label="Sub City"
            name="subCity"
            size="xl"
            class="my-4"
            required="true"
          >
            <USelect v-model="subCity" :options="subCities" />
          </UFormGroup>
          <UFormGroup label="Woreda" name="woreda" size="xl" class="my-4">
            <USelect v-model="woreda" :options="woredas" />
          </UFormGroup>
        </div>
      </UForm>
    </div>
  </div>

  <div class="bg-white rounded-md shadow-md w-full h-fit mb-10">
    <div
      class="p-5 flex justify-start items-center text-slate-600 border-b border-slate-300"
    >
      <h1>Map</h1>
    </div>
    <div>
      <!-- <div ref="google_map" id="map" class="w-1/2 h-[400px]"></div> -->
    </div>
  </div>
</template>

<script setup>
// import { ref } from 'vue';
const cities = [
  "None",
  "Addis Ababa",
  "Awassa",
  "Aswan",
  "Dar es Salaam",
  "Djibouti",
  "Kampala",
  "Nairobi",
  "Mogadishu",
  "Port Harcourt",
  "Tripoli",
  "Tunis",
  "Zanzibar",
  "Zimbabwe",
];
const subCities = ["None", "Bole", "Arada", "Akaki", "Yeka"];
const woredas = ["None", "1", "2", "3", "4"];

const state = reactive({
  address: "",
  city: "",
  subCity: "",
  woreda: "",
});

const google_map = ref(null);

// onMounted(() => {
//   new window.google.maps.Map(google_map.value, {
//     center: { lat: 9.005401, lng: 38.722200 },
//     zoom: 2,
//   });
// });

// const validate = (form) => {
//   return {
//     address: form.address.length > 0,
//     city: form.city.length > 0,
//     subCity: form.subCity.length > 0,
//     woreda: form.woreda.length > 0,
//   };
// };
</script>
