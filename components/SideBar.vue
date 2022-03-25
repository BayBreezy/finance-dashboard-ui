<template>
  <aside class="w-60 border-r hidden md:block border-gray-200 relative">
    <div class="mt-14 ml-8 mb-10">
      <svg-icon name="dots" class="w-10 h-10 text-slate-500" />
    </div>

    <div class="flex flex-col space-y-5">
      <div v-for="(n, i) in nav" :key="`navItem${i}`">
        <NavItem :text="n.text" :icon="n.icon" />
      </div>
    </div>

    <div class="absolute bottom-4 inset-x-0">
      <div
        class="rounded-2xl border border-gray-200 p-2 w-20 h-20 mx-auto relative"
      >
        <div
          class="absolute bottom-1 -right-1 w-3 h-3 rounded-full bg-green-600"
        ></div>
        <img
          src="https://behonbaker.com/icon.png"
          alt="Behon Baker Image"
          class="object-cover w-full h-full rounded-2xl bg-gray-200"
        />
      </div>
      <p class="text-sm font-bold text-center mt-2">Behon Baker</p>
    </div>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      nav: [
        { text: "Home", icon: "home" },
        { text: "Projects", icon: "trophy" },
        { text: "Billings", icon: "bank" },
        { text: "Team Members", icon: "user" },
        { text: "Stats", icon: "bar" },
        { text: "Settings", icon: "settings" },
      ],
    };
  },
};
</script>

<style></style>
