<template>
  <div class="upcoming-curations">
    <Heading text-heading="Upcoming Curations" />
    <VueSlickCarousel v-bind="settings">
      <div class="curation">
        <div class="live-curations">
          <UpcomingPhoto />
        </div>
        <div class="info">
          <CurationInfo />
        </div>
      </div>
      <div class="curation">
        <div class="live-curations">
          <UpcomingPhoto />
        </div>
        <div class="info">
          <CurationInfo />
        </div>
      </div>
    </VueSlickCarousel>
  </div>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";
import Heading from "@/components/Heading.vue";
import UpcomingPhoto from "@/components/UpcomingPhoto.vue";
import CurationInfo from "@/components/CurationInfo.vue";
import VueSlickCarousel from "vue-slick-carousel";

import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

@Component({
  components: { CurationInfo, UpcomingPhoto, Heading, VueSlickCarousel },
})
export default class UpcomingCurations extends Vue {
  settings = {
    dots: true,
    arrows: false,
    dotsClass: "slick-dots custom-dot-class",
    edgeFriction: 0.35,
    infinite: true,
    speed: 1500,
    autoplay: true,
    slidesToShow: 1,
    slidesToScroll: 1,
  };
}
</script>

<style lang="scss" scoped>
.upcoming-curations {
  margin-bottom: 40px;
  width: 100% !important;
}

.live-curations {
  height: 300px;
  width: 40%;
  order: 1;
}

.info {
  order: 2;
  background-color: inherit;
}

.heading {
  order: 3;
}

.curation {
  display: flex !important;
  justify-content: center;
  padding: 100px 35px;
  width: 100%;
  background-color: pink;
}

.slick-dots:before, .custom-dot-class:before {
  font-size: 0;
  line-height: 0;
  display: block;
  width: 10px;
  height: 10px;
  padding: 0;
  min-width: 0;
  cursor: pointer;
  color: transparent;
  border: 2px solid #fff;
  outline: none;
  background: transparent;
  border-radius: 10px;
  transition: all 150ms;
}

@media (max-width: 945px) {
  .curation {
    flex-direction: column;
  }

  .live-curations {
    display: none;
  }
}

@media (max-width: 945px) {
  .curation {
    padding: 20px 35px;
  }
}
</style>
