<template>
  <section class="announcement">
    <div class="page">
      <div class="container">
        <div class="announcement-text">
          {{ text }}
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

@Component
export default class Announcement extends Vue {
  @Prop({ required: true }) private text!: string;
}
</script>

<style lang="scss">
.announcement {
  color: #000000;
  background-color: #f2f2f2;
  text-align: center;
  padding: 7.5px 0;
  font-size: 0.8666rem;
}
.page {
  width: 100%;
  max-width: 100%;
  background-color: transparent;
  margin: 0 auto;
}

.container {
  padding-left: 0;
  padding-right: 0;
  margin: 0 auto;
}

.announcement-text {
  display: inline-block;
  font-family: "Trade", sans-serif;
  font-size: 14px;
  padding: 0 15px 0 15px;
}
</style>
