<template>
  <div class="curation-info">
    <div class="headings">
      <h3 class="heading-text-sm">a live curations with</h3>
      <h1 class="heading-text-bg">Maristella Gonzales</h1>
    </div>
    <div class="slide-image">
      <div class="photo">
        <img src="../assets/girls.png" alt="photo" />
      </div>
      <span class="image-text"> Live Recording </span>
    </div>
    <div class="text">
      Enter the wonderous world of Showfields. Our mission is to create a better
      way for customers to discover, engage and shop emerging brands and artists
      of tomorrow.
    </div>
    <div class="rsvp">RSVP</div>
  </div>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";

@Component
export default class CurationInfo extends Vue {}
</script>

<style lang="scss" scoped>
.curation-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.heading-text-sm,
.heading-text-bg,
.text {
  text-align: center;
  color: #000000;
}

.text,
.heading-text-sm {
  font-family: "Trade Gothic LT Std", sans-serif;
}

.heading-text-sm {
  font-size: 20px;
  line-height: 37px;
  font-weight: bold;
  text-transform: uppercase;
  margin-bottom: 20px;
}

.heading-text-bg {
  width: 619px;
  font-size: 62px;
  line-height: 30px;
  font-family: "Ogg", sans-serif;
  margin-bottom: 30px;
  margin-top: 0;
}

.text {
  width: 300px;
  height: 113px;
  font-size: 16px;
  line-height: 27px;
  margin-bottom: 30px;
}

.rsvp {
  display: block;
  text-align: center;
  margin: 0 45px auto;
  color: #000;
  font-family: "TradeBold", sans-serif;
  position: relative;
  line-height: 1.3;
  padding: 5px 25px 5px 25px;
  border: 1px #000 solid;
  width: 228px;
  height: 31px;
  font-size: 20px;
}

.slide-image {
  display: none;
}

@media (max-width: 945px) {
  .slide-image {
    display: block;
  }

  .slide-image {
    margin-bottom: 15px;
  }

  .text {
    margin-bottom: 20px;
  }

  .rsvp {
    background-color: black;
    color: white;
  }
}

@media (max-width: 945px) {
  .curation-info {
    padding-bottom: 40px;
  }
}

@media (max-width: 600px) {
  .heading-text-bg {
    font-size: 25px;
  }

  .heading-text-sm {
    margin: 0;
    font-size: 16px;
  }

  .text {
    padding: 0 10px 0 10px;
    margin-bottom: 40px;
  }
}
</style>
