<template>
  <div class="flex items-center cursor-pointer group hover:bg-gray-50">
    <div
      class="bg-black h-9 w-1 -translate-x-3 transition-all duration-300 group-hover:translate-x-0"
    ></div>
    <div class="flex items-center space-x-7">
      <svg-icon
        :name="icon"
        class="w-7 h-7 text-gray-600 ml-8 group-hover:text-slate-900 transition-all duration-300"
      />
      <p
        class="text-gray-600 group-hover:text-slate-900 transition-all duration-300"
      >
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
    icon: String,
  },
};
</script>

<style></style>
