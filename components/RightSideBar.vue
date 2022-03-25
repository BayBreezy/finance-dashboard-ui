<template>
  <aside class="h-screen hidden xl:block w-72 lg:py-5 lg:pl-1 lg:pr-5">
    <div
      class="h-full rounded-[2rem] bg-black text-white pl-10 pt-8 relative overflow-hidden"
    >
      <h1 class="font-semibold text-xl mb-8">Sales Revenue</h1>
      <div class="space-y-10">
        <template v-for="(n, i) in nav">
          <div :key="`rightNav-${i}`" class="flex space-x-7 items-center">
            <div
              class="w-12 h-12 rounded-full p-2 bg-white flex items-center justify-center"
            >
              <svg-icon :name="n.icon" class="w-6 h-6 text-black" />
            </div>
            <div>
              <h2 class="font-bold text-xl">{{ n.title }}</h2>
              <p class="text-sm text-gray-400">{{ n.text }}</p>
            </div>
          </div>
        </template>
      </div>

      <!-- Polka Dots -->
      <div
        class="bg-[url('/polka-dots.png')] bg-repeat w-full h-1/3 absolute bottom-0 left-0"
      >
        <div
          class="h-full w-full bg-gradient-to-t from-transparent to-black"
        ></div>
      </div>
    </div>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      nav: [
        { icon: "discount", title: "230k", text: "Sales" },
        { icon: "user-circle", title: "8.549k", text: "Customers" },
        { icon: "column", title: "1.423k", text: "Products" },
        { icon: "pie", title: "$9745", text: "Revenue" },
      ],
    };
  },
};
</script>

<style></style>
