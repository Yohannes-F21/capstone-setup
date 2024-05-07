<template>
  <div
    class="bg-[#e2e2e2] bg-[linear-gradient(to_right,_#e2e2e2,_#c9d6ff)] flex flex-col justify-center items-center h-screen"
  >
    <div
      class="bg-#fff rounded-3xl shadow-xl relative overflow-hidden w-[60%] max-w-[100%] min-h-[480px]"
      id="container"
    >
      <div>
        <div class="form-container absolute top-0 h-full">
          <form
            class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full w-full"
          >
            <h1 class="text-3xl font-bold text-black">Create Account</h1>
            <div
              class="social-icons gap-6 flex justify-start items-center border rounded-md border-[#ccc] w-[70%] mt-5 mb-2 p-1"
            >
              <a href="#" class="icon"><IconsGoogle /></a>
              <p class="text-[#333]">Sign Up with Google</p>
            </div>
            <span class="text-xs">or use your email for registeration</span>
            <!-- <input
              class="bg-[#eee] border-none my-2 py-2.5 px-3.5 text-sm rounded-lg w-full outline-none"
              type="text"
              placeholder="Name"
            />
            <input type="email" placeholder="Email" />
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

            <button
              class="bg-[#512da8] text-[#fff] text-xs py-2.5 px-11 border border-transparent border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
            >
              Sign Up
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style></style>
