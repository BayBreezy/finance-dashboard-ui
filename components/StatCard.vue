<template>
  <div
    :style="{ backgroundColor: c.bg }"
    class="rounded-[2rem] bg-[#000] px-8 py-9 relative"
  >
    <div class="absolute top-7 right-8">
      <svg-icon
        :name="c.up ? 'arrow-up' : 'arrow-down'"
        class="w-5 h-5"
        :style="{ color: c.arrow }"
      />
    </div>
    <div class="flex items-center">
      <div class="flex-1">
        <h1 class="font-bold text-2xl mb-2">{{ c.heading }}</h1>
        <p class="text-sm text-gray-400 truncate">{{ c.sub }}</p>
        <p class="font-bold text-4xl mt-3">{{ c.stat }}</p>
      </div>
      <div @click="toggle" class="mr-5 cursor-pointer">
        <client-only>
          <ProgressBar
            :progress="c.value"
            thickness="7%"
            :loading="loading"
            emptyThickness="7%"
            emptyColor="transparent"
            color="#000"
            :size="110"
          >
            <span class="font-bold text-2xl">{{ c.value }}%</span>
          </ProgressBar>
        </client-only>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    c: Object,
  },
  data() {
    return {
      loading: false,
    };
  },
  methods: {
    toggle() {
      this.loading = true;
      setTimeout(() => {
        this.loading = false;
      }, 1000);
    },
  },
};
</script>

<style></style>
