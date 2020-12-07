<template>
  <div id="app">
    <Header />
    <LiveCurations />
    <UpcomingCurations />
    <RecentCurations />
    <Footer />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Header from "@/components/Header.vue";
import LiveCurations from "@/components/LiveCurations.vue";
import RecentCurations from "@/components/RecentCurations.vue";
import UpcomingCurations from "@/components/UpcomingCurations.vue";
import Footer from "@/components/Footer.vue";

@Component({
  components: {
    Footer,
    UpcomingCurations,
    RecentCurations,
    LiveCurations,
    Header,
  },
})
export default class App extends Vue {}
</script>

<style>
@import "fonts.scss";

* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
