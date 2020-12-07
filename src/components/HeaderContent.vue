<template>
  <div class="header-content">
    <UtilsBar />
    <Navbar />
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import Navbar from "@/components/Navbar.vue";
import UtilsBar from "@/components/UtilsBar.vue";

@Component({
  components: { Navbar, UtilsBar },
})
export default class HeaderContent extends Vue {}
</script>

<style lang="scss">
.header-content {
  margin: 0 auto;
  padding: 0;
}
</style>
