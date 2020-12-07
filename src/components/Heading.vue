<template>
  <div class="heading-text">
    <h1>
      {{ textHeading }}
    </h1>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

@Component
export default class Heading extends Vue {
  @Prop({ required: true }) private textHeading!: string;
}
</script>

<style lang="scss" scoped>
.heading-text {
  display: inline-block;
  padding: 40px 0 40px 0;

  h1 {
    font-size: 36px;
    line-height: 40px;
    font-weight: 400;
    margin: 0;
    color: #000000;
    font-family: "Ogg", sans-serif;
    text-align: center;
  }
}

.heading-text:last-child {
  padding: 0;
}

@media (max-width: 500px) {
  .heading-text {
    h1 {
      font-size: 25px;
    }
  }
}
</style>
