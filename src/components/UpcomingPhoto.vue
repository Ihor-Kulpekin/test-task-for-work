<template>
  <div class="slide-image">
    <div class="photo">
      <img src="../assets/girls.png" alt="photo" />
    </div>
    <span class="image-text"> Live Recording </span>
  </div>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";

@Component
export default class UpcomingPhoto extends Vue {}
</script>

<style lang="scss">
.slide-image {
  position: relative;
  text-align: center;
}

.photo {
  position: relative;
  margin-bottom: 20px;
  img {
    width: 215px;
    height: 215px;
    border-radius: 50%;
    overflow: auto;
    margin: auto;
    position: absolute;
    top: 45px;
    left: 53px;
  }
}

.photo:before {
  content: "";
  background-image: url("../assets/circle.png");
  background-size: 320px;
  background-repeat: no-repeat;
  width: 100%;
  height: 320px;
  display: block;
  margin: 0 auto;
}

.image-text {
  display: block;
  text-align: center;
  margin: 0 45px auto;
  color: #000;
  font-family: "TradeBold", sans-serif;
  position: relative;
  line-height: 1.3;
  padding: 5px 25px 5px 25px;
  border: 1px #000 solid;
  border-radius: 12px;
  width: 228px !important;
  height: 31px;
  font-size: 16px !important;
}

.image-text:after {
  content: "";
  position: absolute;
  left: 10px;
  top: 7px;
  width: 12px;
  height: 12px;
  background: #b3f695;
  border-radius: 50%;
}

@media (max-width: 945px) {
  .slide-image {
    display: none;
  }
}
</style>
