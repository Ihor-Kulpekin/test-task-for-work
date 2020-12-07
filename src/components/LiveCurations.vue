<template>
  <div class="curations">
    <h1 class="heading">Live Curations</h1>
    <div class="curations-text">
      <p class="paragraph">
        Our weekly live curations are one-of-a-kind live shopping events hosted
        by tastemakers from around the globe. We invite you to their worlds to
        give you an interactive and informative shopping experience. These
        curations feature hand-picked products and art from the most interesting
        misson-driven, design-oriented, innovative brands and artists in our
        community.
      </p>
    </div>
  </div>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";

@Component
export default class LiveCurations extends Vue {}
</script>

<style lang="scss">
.curations {
  width: 100%;
  max-width: 100%;
  text-align: center;
  color: #ffffff;
  background-color: black;
}

.heading {
  font-size: 61px;
  line-height: 63px;
  font-family: "Ogg", sans-serif;
  padding-top: 50px;
}

.paragraph {
  line-height: 27px;
  max-width: 834px;
  margin-bottom: 50px;
  font-family: "Trade Gothic LT Std", sans-serif;
  padding: 0 20px 0 20px;
}

.curations-text {
  display: inline-block;
  font-family: "Trade", sans-serif;
  font-size: 16px;
  word-wrap: break-word;
}


@media (max-width: 500px) {
  .heading {
    font-size: 25px;
    padding-top: 10px;
  }

  .paragraph {
    font-size: 16px;
  }
}
</style>
