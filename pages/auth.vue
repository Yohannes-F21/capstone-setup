<template>
  <div class="page">
    <div
      class="bg-#fff rounded-3xl shadow-xl relative overflow-hidden w-[60%] max-w-[100%] min-h-[480px]"
      id="container"
    >
      <!-- <div
        class="form-container absolute top-0 h-full transition duration-700 ease-in-out sign-up left-0 w-1/2 z-[1] opacity-0 active:transform active:translate-x-full active:opacity-[1] active:z-[5] active:animate-pulse"
      >
        <form
          class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full"
        >
          <h1>Create Account</h1>
          <div class="social-icons my-5">
            <a
              href="#"
              class="icon border border-[#ccc] rounded-[20%] inline-flex justify-center items-center my-1 w-10 h-10"
              ><i class="fa-brands fa-google-plus-g"></i
            ></a>
            <a
              href="#"
              class="icon border border-[#ccc] rounded-[20%] inline-flex justify-center items-center my-1 w-10 h-10"
              ><i class="fa-brands fa-facebook-f"></i
            ></a>
            <a
              href="#"
              class="icon border border-[#ccc] rounded-[20%] inline-flex justify-center items-center my-1 w-10 h-10"
              ><i class="fa-brands fa-github"></i
            ></a>
            <a
              href="#"
              class="icon border border-[#ccc] rounded-[20%] inline-flex justify-center items-center my-1 w-10 h-10"
              ><i class="fa-brands fa-linkedin-in"></i
            ></a>
          </div>
          <span class="text-xs">or use your email for registeration</span>
          <input
            class="bg-[#eee] border-none my-2 py-2.5 px-3.5 text-sm rounded-lg w-full outline-none"
            type="text"
            placeholder="Name"
          />
          <input type="email" placeholder="Email" />
          <input type="password" placeholder="Password" />
          <button
            class="bg-[#512da8] text-[#fff] text-xs py-2.5 px-11 border border-transparent border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
          >
            Sign Up
          </button>
        </form>
      </div> -->
      <div class="form-container absolute top-0 h-full sign-in left-0 w-1/2">
        <form
          class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full w-full"
        >
          <h1 class="text-3xl font-bold text-black">Sign In</h1>
          <div
            class="social-icons gap-6 flex justify-start items-center border rounded-md border-[#ccc] w-[70%] mt-5 mb-2 p-1"
          >
            <a href="#" class="icon"><IconsGoogle /></a>
            <p class="text-[#333]">Sign In with Google</p>
          </div>
          <span class="text-[#333] text-xs">or use your email password</span>
          <!-- <input type="email" placeholder="Email" />
          <input type="password" placeholder="Password" /> -->

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
            <!-- <input type="text" class="border border-gray-300 bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-400 focus:border-transparent rounded-md py-2 px-4 w-full"> -->

            <!-- <UButton type="submit"> Submit </UButton> -->
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
          <!-- <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0 transform translate-x-0 transition duration-700 ease-in-out toggle-left active:translate-x-[-200%]"
          >
            <h1>Welcome Back!</h1>
            <p class="text-sm leading-5 tracking-[0.3px] my-5">
              Enter your personal details to use all of site features
            </p>
            <button
              class="bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
              id="login"
            >
              Sign In
            </button>
          </div> -->
          <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0 transform translate-x-0 transition duration-700 ease-in-out"
          >
            <h1 class="text-2xl font-bold">Hello, Friend!</h1>
            <p>
              Register with your personal details to use all of site features
            </p>
            <button
              class="bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
              id="register"
            >
              Sign Up
            </button>
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
<style lang="css" scoped>
.page {
  background-color: #e2e2e2;
  background: linear-gradient(to right, #e2e2e2, #c9d6ff);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
}
</style>
