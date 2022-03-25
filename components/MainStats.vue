<template>
  <div
    class="p-10 bg-[#F9F8F3] grid grid-cols-2 lg:grid-cols-3 gap-x-3 gap-y-5 rounded-3xl"
  >
    <template v-for="(stat, i) in stats">
      <div :key="`mainStat-${i}`">
        <div class="p-3 inline-block rounded-full bg-[#E4E0D6]">
          <svg-icon :name="stat.icon" class="w-6 h-6" />
        </div>
        <p class="mt-5 text-sm text-gray-400">{{ stat.subText }}</p>
        <h1 class="font-bold text-5xl mt-3 mb-5">{{ stat.stat }}</h1>
        <p class="text-sm text-gray-400">{{ stat.interval }}</p>
      </div>
    </template>
  </div>
</template>

<script>
export default {
  data() {
    return {
      stats: [
        { icon: "eye", stat: 500, subText: "Views", interval: "Per Day" },
        {
          icon: "compass",
          stat: 2000,
          subText: "Visits",
          interval: "Per Minutes",
        },
        { icon: "store", stat: 5100, subText: "Orders", interval: "Per Day" },
      ],
    };
  },
};
</script>

<style></style>
