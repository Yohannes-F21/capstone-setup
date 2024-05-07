<template>
  <div class="page">
    <div
      class="bg-#fff rounded-3xl shadow-lg relative overflow-hidden w-[60%] max-w-[100%] min-h-[480px]"
      id="container"
    >
      <div
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
      </div>
      <div
        class="form-container absolute top-0 h-full transition duration-700 ease-in-out sign-in left-0 w-1/2 z-[2] active:transform active:translate-x-full"
      >
        <form
          class="bg-[#fff] flex items-center justify-center flex-col px-10 h-full"
        >
          <h1>Sign In</h1>
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
          <span>or use your email password</span>
          <input type="email" placeholder="Email" />
          <input type="password" placeholder="Password" />
          <a href="#" class="text-[#333] text-sm no-underline mt-3.5 mb-2.5"
            >Forget Your Password?</a
          >
          <button
            class="bg-[#512da8] text-[#fff] text-xs py-2.5 px-11 border border-transparent border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
          >
            Sign In
          </button>
        </form>
      </div>
      <div
        class="toggle-container absolute top-0 left-1/2 w-1/2 h-full overflow-hidden transition duration-700 ease-in-out rounded rounded-tl-[150px] rounded-bl-[100px] z-[1000] active:transform active:translate-x-[-100%] active:rounded-tr-[150px] rounded-br-[100px]"
      >
        <div
          class="toggle bg-[#512da8] h-full text-[#fff] relative left-[-100] w-[200%] transform translate-x-0 transition duration-700 ease-in-out active:transform active:translate-x-[50%]"
        >
          <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0 transform translate-x-0 transition duration-700 ease-in-out toggle-left active:translate-x-[-200%]"
          >
            <h1>Welcome Back!</h1>
            <p class="text-sm leading-5 tracking-[0.3px] my-5">
              Enter your personal details to use all of site features
            </p>
            <button
              class="hidden bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
              id="login"
            >
              Sign In
            </button>
          </div>
          <div
            class="toggle-panel absolute w-1/2 h-full flex items-center justify-center flex-col px-8 text-center top-0 transform translate-x-0 transition duration-700 ease-in-out toggle-right right-0 active:translate-x-[200%]"
          >
            <h1>Hello, Friend!</h1>
            <p>
              Register with your personal details to use all of site features
            </p>
            <button
              class="hidden bg-transparent text-[#fff] text-xs py-2.5 px-11 border border-[#fff] border-solid rounded-lg font-semibold tracking-wider uppercase mt-2.5 cursor-pointer"
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

<script setup></script>
<style lang="css" scoped>
.page {
  background-color: #c9d6ff;
  /* background: linear-gradient(to right, #e2e2e2, #c9d6ff); */
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
}
</style>
