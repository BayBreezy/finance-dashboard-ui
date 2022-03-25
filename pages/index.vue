<template>
  <div>
    <div class="flex w-full h-screen">
      <SideBar />
      <main class="overflow-y-auto flex-1 min-h-screen">
        <div class="pt-14 lg:px-16 md:px-5 px-5">
          <div class="h-screen w-full col-span-9">
            <!-- Search Input -->
            <SearchInput />
            <WelcomeFilter />
            <br />
            <MainStats />
            <br /><br />
            <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-rows-2 gap-5">
              <template v-for="(c, n) in cards">
                <StatCard :key="`statCard-${n}`" :c="c" />
              </template>
            </div>
            <br /><br />
          </div>
        </div>
      </main>
      <RightSideBar />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          heading: "Sales",
          sub: "Total sales today",
          stat: "$500",
          value: 55,
          bg: "#FFEDE3",
          arrow: "#D57E4D",
        },
        {
          heading: "Profit",
          sub: "Per day ratio",
          stat: "$150",
          value: 30,
          bg: "#EEFCF0",
          arrow: "#81CE88",
        },
        {
          heading: "Orders",
          sub: "Total orders today",
          stat: "1000",
          value: 80,
          up: true,
          bg: "#E6F5FA",
          arrow: "#77C4D8",
        },
        {
          heading: "Visits",
          sub: "Total visits today",
          stat: "400",
          value: 70,
          up: true,
          bg: "#F4F5F9",
          arrow: "#000000",
        },
      ],
    };
  },
};
</script>
