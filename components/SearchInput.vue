<template>
  <div class="flex items-center">
    <div
      class="md:hidden flex items-center justify-center border p-3 mr-2 rounded-lg cursor-pointer"
    >
      <svg-icon name="menu-left" class="w-5 h-5 text-gray-600" />
    </div>
    <div class="w-full relative">
      <div class="absolute left-3 inset-y-0 mx-auto flex items-center">
        <svg-icon name="search" class="h-5 w-5" />
      </div>
      <label for="search-stat" class="sr-only">Search for stats</label>
      <input
        type="search"
        id="search-stat"
        name="search-stat"
        class="outline-none w-full placeholder:text-slate-400 placeholder:text-sm text-sm border pl-10 border-slate-300 py-3 px-2 rounded-lg focus:border-primary-500"
        placeholder="Search for stats"
      />
    </div>
    <div
      class="xl:hidden flex items-center justify-center border p-3 ml-2 rounded-lg cursor-pointer"
    >
      <svg-icon name="menu-right" class="w-5 h-5 text-gray-600" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
