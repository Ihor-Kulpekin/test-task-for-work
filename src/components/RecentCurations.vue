<template>
  <div class="recentCurations">
    <div class="heading">
      <Heading text-heading="Watch Recent Live Curations" />
    </div>
    <div class="curators">
      <div class="curators-amount">
        <div class="curators-item">
          <a href="/">
            <img class="topLeft" src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/Triangle.png?v=1592897170" alt="trianlge">
            <img
              class="bg_img front-image"
              data-src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/Polygon.png?v=1592897409"
              src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/1111_100x100.png?v=1594727255"
            />
            <img
              class="img"
              data-src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/kilolo_x200.png?v=1606492662"
              src="../assets/goodGirl.png"
            />
          </a>
          <h3>Kilolo Lucket</h3>
        </div>
        <div class="curators-item">
          <a href="/">
            <img
              class="img"
              data-src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/kilolo_x200.png?v=1606492662"
              src="../assets/secondGirl.png"
            />
          </a>
          <h3>Lauren Mazzei</h3>
        </div>
        <div class="curators-item">
          <a href="/">
            <img
              class="bg_img right-top"
              src="../assets/Polygon@3x.png"
            />
            <img
              class="img"
              src="../assets/Background@3x.png"
            />
          </a>
          <h3>Caleb Thill</h3>
        </div>
        <div class="curators-item">
          <a href="/">
            <img
              class="bg_img right-top"
              data-src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/Polygon.png?v=1592897409"
              src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/Polygon.png?v=1592897409"
            />
            <img
              class="img"
              data-src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/kilolo_x200.png?v=1606492662"
              src="//cdn.shopify.com/s/files/1/0302/8520/1452/files/kilolo_x200.png?v=1606492662"
            />
          </a>
          <h3>Kilolo Lucket</h3>
        </div>
        <div class="curators-item">
          <a href="/">
            <img
              class="yellow-line"
              src="../assets/yellow_line.png"
            />
            <img
              class="img"
              src="../assets/thirdGirl.png"
            />
          </a>
          <h3>Kilolo Lucket</h3>
        </div>
        <div class="curators-item">
          <a href="/">
            <img
              class="img"
              src="../assets/boy.png"
            />
          </a>
          <h3>Nick Pinsker</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import Heading from "@/components/Heading.vue";
@Component({
  components: { Heading },
})
export default class RecentCurations extends Vue {}
</script>

<style lang="scss" scoped>
h3 {
  font-size: 36px;
  font-family: "OGG";
  padding-top: 15px;
  font-weight: 400;
}

.recentCurations {
  margin: 30px auto 50px auto;
  width: 100%;
  max-width: 1280px;
}

.heading {
  padding: 0;
  margin-bottom: 50px;
}

.curators {
  text-align: center;
  padding: 0 20px 0 20px;
}

.curators-amount {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 60px;
}

.curators-item {
  position: relative;
  text-align: center;
  background: url(//cdn.shopify.com/s/files/1/0302/8520/1452/t/14/assets/polaroid-bg.png?v=659069652087436824)
    no-repeat top center;
  background-size: 160px 195px;
}

.bg_img, .topLeft, .right-top, .yellow-line{
  position: absolute;
  z-index: -1;
}

.yellow-line {
  left: 50%;
}

.right-top {
  top: -30px;
  right: 45px;
  z-index: -1;
}

@keyframes swing {
  0%, 100% { transform: rotate(-10deg); }
  20% {transform:scale(.95);}
  50% { transform: rotate(10deg); }
  80% {transform:scale(.95);}
}

.front-image {
  top: -45px;
  left: 25px;
  z-index: 2;
  position: absolute;
  animation: swing;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
}

.topLeft {
  top: -60px;
  left: 60px;
}

.img {
  z-index: 1;
}

.img, .right-top {
  margin: 10px 0px 10px 0px;
  width: 140px;
  height: 160px;
  object-fit: cover;
}

.yellow-line {
  top: -28px;
  left: 80px;
  width: 177px;
  height: 266px;
}

@media (max-width: 1024px) {
  .curators-amount {
    grid-gap: 40px;
  }

  .right-top {
    right: 20px;
  }
}

@media (max-width: 768px) {
  .curators-amount {
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
  }

  .front-image {
    left: -5px;
  }

  .yellow-line {
    left: 25px;
  }
}

@media (max-width: 500px) {
  h3 {
    font-size: 16px;
  }

  .img {
    max-width: 90%;
    max-height: 90%;
    margin: 7px 0px 10px 0px;
  }

  .topLeft {
    display: none;
  }

  .front-image {
    display: none;
  }

  .yellow-line {
    left: 0;
    width: 140px;
    height: 220px;
  }
}
</style>
