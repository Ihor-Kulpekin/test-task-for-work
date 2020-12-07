<template>
  <div class="header">
    <Announcement
      text="COVID-19: Learn what we’re doing to keep the community and our staff safe."
    />
    <HeaderContent />
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

import Announcement from "@/components/Announcement.vue";
import HeaderContent from "@/components/HeaderContent.vue";

@Component({
  components: {
    HeaderContent,
    Announcement,
  },
})
export default class Header extends Vue {}
</script>

<style lang="scss" scoped>
.header {
  margin: 0 auto 0 auto;
  width: 100%;
  background-color: rgba(0, 0, 0, 0);
}
</style>
