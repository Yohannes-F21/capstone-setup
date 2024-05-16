<template>
  <div class="w-[19%] h-screen bg-[#2d2774] flex text-[#839EA8]">
    <div
      class="[text-decoration:none] flex-1 flex flex-col items-start justify-start my-16"
    >
      <template v-for="{ icon, path, label } in sidebarLinks" :key="label">
        <NuxtLink
          class="flex items-center gap-4 my-4 mx-6 hover:text-white"
          :to="path"
        >
          <span>
            <component :is="icon" class="w-5 h-5"></component>
          </span>
          {{ label }}</NuxtLink
        >
      </template>
    </div>
  </div>
</template>
<script setup>
const sidebarLinks = [
  {
    label: "Dashboard",
    icon: resolveComponent("IconsDashboard"),
    path: "/dashboard",
    active: false,
  },
  {
    label: "Insights",
    icon: resolveComponent("IconsInsights"),
    path: "/insights",
    active: false,
  },
  {
    label: "Properties",
    icon: resolveComponent("IconsProperties"),
    path: "/properties",
    active: false,
  },
  {
    label: "Create a Listing",
    icon: resolveComponent("IconsList"),
    path: "/create-listing",
    active: false,
  },
  {
    label: "Favorites",
    icon: resolveComponent("IconsFavorites"),
    path: "/favorites",
    active: false,
  },
  {
    label: "Saved Searches",
    icon: resolveComponent("IconsSearch"),
    path: "/saved-searches",
    active: false,
  },
  {
    label: "Messages",
    icon: resolveComponent("IconsMessage"),
    path: "/messages",
    active: false,
  },
  {
    label: "My Profile",
    icon: resolveComponent("IconsProfile"),
    path: "/profile",
    active: false,
  },
  {
    label: "Log Out",
    icon: resolveComponent("IconsKey"),
    path: "/",
    active: false,
  },
];
</script>

<style>
.router-link-active {
  @apply text-white;
}
.router-link-exact-active {
  @apply text-white;
}
</style>
