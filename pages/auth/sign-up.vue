<template>
  <div
    class="bg-[#e2e2e2] bg-[linear-gradient(to_right,_#e2e2e2,_#c9d6ff)] flex flex-col justify-center items-center h-screen"
  >
    <div
      class="bg-#fff rounded-3xl shadow-xl relative overflow-hidden w-[60%] max-w-[100%] min-h-[480px]"
      id="container"
    >
      <div>
        <div class="form-container absolute top-0 h-full right-0 w-1/2">
          <form
            class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full w-full"
          >
            <h1 class="text-3xl font-bold text-black">Create Account</h1>
            <div
              class="social-icons gap-6 flex justify-start items-center border rounded-md border-[#ccc] w-[70%] mt-5 mb-2 p-1"
            >
              <a href="#" class="icon"><IconsGoogle /></a>
              <p class="text-[#333] text-sm">Sign Up with Google</p>
            </div>
            <span class="text-xs">or use your email for registeration</span>

            <UForm
              :validate="validate"
              :state="state"
              class="space-y-3 w-full"
              @submit="onSubmit"
            >
              <UFormGroup class="" label="" name="firstName">
                <UInput
                  v-model="state.firstName"
                  placeholder="First Name"
                  class="rounded-md py-1 px-3 w-full"
                />
              </UFormGroup>
              <UFormGroup class="" label="" name="lastName">
                <UInput
                  v-model="state.lastName"
                  placeholder="Last Name"
                  class="rounded-md py-1 px-3 w-full"
                />
              </UFormGroup>

              <UFormGroup label="" name="Phone">
                <UInput
                  v-model="state.phone"
                  placeholder="Phone"
                  class="rounded-md py-1 px-3 w-full"
                />
              </UFormGroup>
              <UFormGroup label="" name="email">
                <UInput
                  v-model="state.password"
                  placeholder="Email"
                  class="rounded-md py-1 px-3 w-full"
                />
              </UFormGroup>
              <UFormGroup label="" name="password">
                <UInput
                  v-model="state.password"
                  type="password"
                  placeholder="Password"
                  class="rounded-md py-1 px-3 w-full"
                />
              </UFormGroup>
            </UForm>

            <button
              class="bg-[#512da8] text-[#fff] text-xs py-2.5 px-11 border border-transparent border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
            >
              Sign Up
            </button>
          </form>
        </div>
      </div>
      <div
        class="toggle-container bg-[#fff] absolute top-0 right-1/2 w-1/2 h-full overflow-hidden transition duration-700 ease-in-out rounded rounded-tr-[150px] rounded-br-[100px] z-[1000]"
      >
        <div
          class="toggle bg-[#7065F0] h-full text-[#fff] relative left-[-100] w-[200%] transform translate-x-0 transition duration-700 ease-in-out"
        >
          <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0"
          >
            <h1>Welcome Back!</h1>
            <p class="text-sm leading-5 tracking-[0.3px] my-5">
              Enter your personal details to use all of site features
            </p>
            <NuxtLink to="sign-in">
              <button
                class="bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
                id="login"
              >
                Sign In
              </button>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
//import type { FormError, FormSubmitEvent } from '#ui/types'

const state = reactive({
  firstName: undefined,
  lastName: undefined,
  phone: undefined,
  email: undefined,
  password: undefined,
});

const validate = () => {
  const errors = [];
  if (!state.email) errors.push({ path: "email", message: "Required" });
  if (!state.password) errors.push({ path: "password", message: "Required" });
  if (!state.firstName) errors.push({ path: "firstName", message: "Required" });
  if (!state.lastName) errors.push({ path: "lastName", message: "Required" });
  if (!state.phone) errors.push({ path: "phone", message: "Required" });
  return errors;
};

async function onSubmit() {
  // Do something with data
  // console.log(event.data)
}
</script>
<style></style>
