<template>
  <div
    class="bg-[#e2e2e2] bg-[linear-gradient(to_right,_#e2e2e2,_#c9d6ff)] flex flex-col justify-center items-center h-screen"
  >
    <div
      class="bg-[#fff] rounded-3xl shadow-xl relative overflow-hidden w-[60%] max-w-[100%] min-h-[480px]"
      id="container"
    >
      <div class="form-container absolute top-0 h-full sign-in left-0 w-1/2">
        <form
          class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full w-full"
        >
          <h1 class="text-3xl font-bold text-black">Sign In</h1>
          <div
            class="social-icons gap-6 flex justify-start items-center border rounded-md bg-[#c9d6ff] border-[#ccc] w-[70%] mt-5 mb-2 p-1"
          >
            <a href="#" class="icon"><IconsGoogle /></a>
            <p class="text-[#333] text-sm">Sign In with Google</p>
          </div>
          <span class="text-[#333] text-xs mb-1"
            >or use your email password</span
          >

          <UForm
            :validate="validate"
            :state="state"
            class="space-y-4 w-full"
            @submit="onSubmit"
          >
            <UFormGroup class="" label="" name="email">
              <UInput
                v-model="state.email"
                placeholder="Email"
                class=""
                input-class="bg-[#e2e2e2] rounded-md py-2 px-3 w-full focus:outline-none focus:border-[#7065F0]"
              />
            </UFormGroup>

            <UFormGroup label="" name="password">
              <UInput
                v-model="state.password"
                type="password"
                placeholder="Password"
                class=""
                input-class="bg-[#e2e2e2] rounded-md py-2 px-3 w-full"
              />
            </UFormGroup>
          </UForm>

          <a href="#" class="text-[#333] text-sm no-underline mt-3.5 mb-2.5"
            >Forget Your Password?</a
          >
          <button
            type="submit"
            class="bg-[#512da8] text-[#fff] text-xs py-2.5 px-11 border border-transparent border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
          >
            Sign In
          </button>
        </form>
      </div>
      <div
        class="toggle-container bg-[#fff] absolute top-0 left-1/2 w-1/2 h-full overflow-hidden transition duration-700 ease-in-out rounded rounded-tl-[150px] rounded-bl-[100px] z-[1000]"
      >
        <div
          class="toggle bg-[#7065F0] h-full text-[#fff] relative left-[-100] w-[200%] transform translate-x-0 transition duration-700 ease-in-out"
        >
          <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0 transform translate-x-0 transition duration-700 ease-in-out"
          >
            <h1 class="text-2xl font-bold">Hello, Friend!</h1>
            <p>
              Register with your personal details to use all of site features
            </p>
            <NuxtLink to="sign-up">
              <button
                class="bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
                id="register"
              >
                Sign Up
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
  email: undefined,
  password: undefined,
});

const validate = () => {
  const errors = [];
  if (!state.email) errors.push({ path: "email", message: "Required" });
  if (!state.password) errors.push({ path: "password", message: "Required" });
  return errors;
};

async function onSubmit() {
  // Do something with data
  // console.log(event.data)
}
</script>
