<template>
  <div>
    <div class="flex justify-between items-end mt-14">
      <div>
        <h1 class="text-3xl font-bold tracking-wide text-slate-900">
          Hello Breezy
        </h1>
        <p class="text-gray-400 mt-2">Welcome Back!</p>
      </div>
      <div>
        <div
          class="border border-slate-300 rounded-lg flex space-x-3 px-4 py-2 group hover:border-primary-400 cursor-pointer"
        >
          <p class="text-slate-500 group-hover:text-primary-800">Filters</p>
          <svg-icon
            name="filter"
            class="w-5 h-5 group-hover:text-primary-800"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
