<template>
  <div
    class="w-[17%] h-screen bg-[#2d2774] flex flex-row justify-start items-start box-border text-left text-[#839EA8]"
  >
    <div
      class="[text-decoration:none] flex-1 flex flex-col items-start justify-start my-16"
    >
      <div
        v-for="{ icon, path, label } in sidebarLinks"
        :key="label"
        class="flex flex-row items-center justify-start gap-4 my-4 mx-6"
      >
        <span>
          <component :is="icon" class="w-3.5 h-3.5"></component>
        </span>
        <div>
          <NuxtLink :to="path">{{ label }}</NuxtLink>
        </div>
      </div>
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
  },
  {
    label: "Log Out",
    icon: resolveComponent("IconsKey"),
    path: "/",
  },
];
</script>
