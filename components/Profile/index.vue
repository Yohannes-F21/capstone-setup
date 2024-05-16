<template>
  <div>
    <div class="w-full min-h-screen">
      <div
        class="w-full px-8 py-4 bg-white flex flex-wrap justify-between items-center box-border text-left text-base text-[#839EA8]"
      >
        <h1 class="text-xl text-black">My Profile</h1>
        <UButton color="indigo" variant="solid" size="xl">
          View Profie In Public
        </UButton>
      </div>
      <div class="p-5 m-2 flex -start items-center text-slate-600 text-lg">
        <h1>Information</h1>
      </div>
      <div
        class="sm:w-[95%] my-6 sm:mx-auto mx-5 bg-white rounded-md shadow-md"
        id="user-information"
      >
        <div class="sm:flex sm:gap-8 p-6" id="container">
          <div class="sm:w-1/4 mx-auto">
            <NuxtImg
              src="https://img.freepik.com/free-vector/blue-circle-with-white-user_78370-4707.jpg?size=626&ext=jpg"
              alt="profile"
              class="rounded-full"
            />
            <UButton
              color="indigo"
              variant="solid"
              size="xl"
              class="sm:w-full mx-auto"
            >
              Update Profile Picture
            </UButton>
          </div>
          <UForm
            :validate="validate"
            :state="state"
            class="w-full"
            @submit="onSubmit"
          >
            <div class="w-full sm:grid sm:grid-cols-2 sm:gap-x-10">
              <UFormGroup label="Email" name="email" size="xl" class="my-4">
                <UInput
                  placeholder="Enter your Email"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup
                label="First Name"
                name="firstName"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder="Enter your First Name"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup
                label="Last Name"
                name="lastName"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder="Enter your Last Name"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup label="Phone" name="phone" size="xl" class="my-4">
                <UInput
                  placeholder="Enter your Phone"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup
                label="Telegram"
                name="telegram"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder="Enter your Telegram User Name"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup
                label="WhatsApp"
                name="WhatsApp"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder="Enter your WhatsApp User Name"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                />
              </UFormGroup>
              <UFormGroup label="About Me" name="bio" size="xl" class="my-4">
                <UTextarea size="xl" placeholder="Enter your bio" resize />
              </UFormGroup>
            </div>
          </UForm>
        </div>
      </div>
      <div
        class="sm:w-[95%] my-6 sm:mx-auto mx-5 bg-white rounded-md shadow-md"
        id="change-password"
      >
        <div class="flex gap-8 p-6">
          <div class="w-1/4 mx-auto">
            <h1>Change Password</h1>
          </div>
          <UForm
            :validate="validate"
            :state="state"
            class="w-full"
            @submit="onSubmit"
          >
            <div class="w-full sm:grid sm:grid-cols-2 sm:gap-x-10">
              <UFormGroup
                label="New Password"
                name="newPassword"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder=" Enter New Password"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                  type="password"
                />
              </UFormGroup>
              <UFormGroup
                label="Confirm New Password"
                name="confirmPassword"
                size="xl"
                class="my-4"
              >
                <UInput
                  placeholder="Confirm New Password"
                  input-class=" rounded-md  w-full "
                  variant="outline"
                  type="password"
                />
              </UFormGroup>
              <UButton
                color="primary"
                variant="solid"
                size="xl"
                class="w-[50%]"
              >
                Update Password</UButton
              >
            </div>
          </UForm>
        </div>
      </div>
      <div
        class="sm:w-[95%] my-6 sm:mx-auto mx-5 bg-white rounded-md shadow-md"
        id="change-password"
      >
        <div class="flex gap-8 p-6">
          <div class="w-1/4 mx-auto">
            <h1>Delete Account</h1>
          </div>

          <div class="w-full sm:grid sm:grid-cols-2 sm:gap-x-10">
            <UButton color="red" variant="solid" size="xl" class="w-[50%]">
              Delete My Account</UButton
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style></style>
