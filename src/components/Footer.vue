<template>
  <footer class="footer">
    <div class="footer-menu">
      <div
        class="footer-menu-item"
        v-on:click="arrayList['firstBlock'].openBlock()"
      >
        <p class="tittle" v-if="arrayList['firstBlock'].isOpen === true">
          about showfields
        </p>
        <p
          class="tittleWithMinus"
          v-if="arrayList['firstBlock'].isOpen === false"
        >
          about showfields
        </p>
        <div
          class="footer-menu-item-list"
          v-bind:class="{
            open: arrayList['firstBlock'].isOpen === false,
            close: arrayList['firstBlock'].isOpen === true,
          }"
        >
          <a href="">About Us</a>
          <a href="">Contact</a>
          <a href="">FAQ</a>
          <a href="">Privacy Policy</a>
          <a href="">Terms Of Service</a>
          <a href="">Gift Card</a>
        </div>
      </div>
      <div
        class="footer-menu-item"
        v-on:click="arrayList['secondBlock'].openBlock()"
      >
        <p class="tittle" v-if="arrayList['secondBlock'].isOpen === true">
          visit us
        </p>
        <p
          class="tittleWithMinus"
          v-if="arrayList['secondBlock'].isOpen === false"
        >
          visit us
        </p>
        <div
          class="footer-menu-item-list"
          v-bind:class="{
            open: arrayList['secondBlock'].isOpen === false,
            close: arrayList['secondBlock'].isOpen === true,
          }"
        >
          <a href="">Locations</a>
          <a href="">Store Appointments</a>
          <a href="">Virtual Appointments</a>
        </div>
      </div>
      <div
        class="footer-menu-item"
        v-on:click="arrayList['thirdBlock'].openBlock()"
      >
        <p class="tittle" v-if="arrayList['thirdBlock'].isOpen === true">
          partner with us
        </p>
        <p
          class="tittleWithMinus"
          v-if="arrayList['thirdBlock'].isOpen === false"
        >
          partner with us
        </p>
        <div
          class="footer-menu-item-list"
          v-bind:class="{
            open: arrayList['thirdBlock'].isOpen === false,
            close: arrayList['thirdBlock'].isOpen === true,
          }"
        >
          <a href="">Artists</a>
          <a href="">Brand Partnerships</a>
          <a href="">Careers</a>
        </div>
      </div>
      <div
        class="footer-menu-item"
        v-on:click="arrayList['fourthBlock'].openBlock()"
      >
        <p class="tittle" v-if="arrayList['fourthBlock'].isOpen === true">
          find us
        </p>
        <p
          class="tittleWithMinus"
          v-if="arrayList['fourthBlock'].isOpen === false"
        >
          find us
        </p>
        <div
          class="footer-menu-item-list"
          v-bind:class="{
            open: arrayList['fourthBlock'].isOpen === false,
            close: arrayList['fourthBlock'].isOpen === true,
          }"
        >
          <a href="">Instagram</a>
          <a href="">Pinterest</a>
          <a href="">Facebook</a>
          <a href="">Twitter</a>
        </div>
      </div>
      <div class="footer-menu-item">
        <p class="tittle">
          STAY IN THE KNOW! SUBSCRIBE TO OUR NEWSLETTER. PLUS, RECEIVE 10% OFF
          YOUR FIRST ORDER.
        </p>
        <div class="footer-input">
          <input
            type="email"
            class="input"
            placeholder="Enter your email to subscribe"
          />
          <button class="noshowing">submit</button>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="js">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class Footer extends Vue {
  arrayList = {
    'firstBlock': {
      isOpen: true,
      openBlock: function () {
        this.isOpen = !this.isOpen;
      }
    },
    'secondBlock': {
      isOpen: true,
      openBlock: function () {
        this.isOpen = !this.isOpen;
      }
    },
    'thirdBlock':{
      isOpen: true,
      openBlock: function () {
        this.isOpen = !this.isOpen;
      }
    },
    'fourthBlock': {
      isOpen: true,
      openBlock: function () {
        this.isOpen = !this.isOpen;
      }
    }
  }
}
</script>

<style lang="scss" scoped>
input {
  background-color: #fff;
  color: #000;
  border: 1px solid rgba(0, 0, 0, 0.15);
  font-family: "Trade Gothic LT Std", serif;
  font-weight: 400;
  font-style: normal;
  max-width: 100%;
  padding: 10px;
  margin: 5px 5px 5px 0;
  border-radius: 0;
  touch-action: manipulation;
}

.footer {
  display: flex;
  justify-content: center;
  padding: 80px 15px 70px 15px;
  background-color: #f2f2f2;
  overflow: hidden;
}

.footer-menu {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-wrap: wrap-reverse;
  margin: 0 auto;
  width: 1024px;
  max-width: 100%;
}

.footer-menu-item-list {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  a {
    text-decoration: none;
    margin-bottom: 5px;
    text-align: left;
    color: #000;
    font-family: "Trade Gothic LT Std", sans-serif;
  }
}

.footer-menu-item:nth-child(1) {
  order: 1;
}

.footer-menu-item:nth-child(2) {
  order: 2;
}
.footer-menu-item:nth-child(3) {
  order: 3;
}

.footer-menu-item:nth-child(4) {
  order: 4;
}

.footer-menu-item:nth-child(5) {
  order: 24;
}

.tittle {
  font-size: 11px;
  font-family: "Trade Gothic LT Std", sans-serif;
  color: #000;
  line-height: 15px;
  max-width: 260px;
  text-transform: uppercase;
  text-align: left;
  font-weight: bold;
}

.tittleWithMinus {
  @extend .tittle;
}

.footer-input {
  position: relative;
  .input {
    background: transparent;
    border: none;
    padding-left: 0;
    padding-top: 0;
    border-bottom: 2px #000 solid;
    outline: none;
    width: 100%;
    font-size: 11px;
    font-family: "Trade Gothic LT Std", sans-serif;
  }
}

.noshowing {
  position: absolute;
  right: -40px;
  bottom: 5px;
  width: 13px !important;
  height: 32px;
  font-size: 7px;
  display: block;
  transform: scale(0.6);
  opacity: 0;
}

@media (max-width: 800px) {
  .footer {
    padding: 25px 0px 10px 0px;
  }

  .footer-menu-item {
    width: 100%;
    border-bottom: 2px #000 solid;
    padding: 0px 30px;
  }

  .footer-menu-item:nth-child(5) {
    :after {
      content: "";
    }
  }

  .tittle {
    position: relative;
    max-width: 100%;
    width: 100%;
  }

  .footer-menu-item:nth-child(1) {
    order: 5;
  }

  .footer-menu-item:nth-child(2) {
    order: 4;
  }
  .footer-menu-item:nth-child(3) {
    order: 3;
  }

  .footer-menu-item:nth-child(4) {
    order: 2;
  }

  .footer-menu-item:nth-child(5) {
    padding-bottom: 30px;
  }

  .tittleWithMinus:after,
  .tittle:after {
    position: absolute;
    right: 10px;
    top: 0;
    font-size: 20px;
    line-height: 15px;
    color: #000;
  }

  .tittle:after {
    content: "+";
  }

  .tittleWithMinus:after {
    content: "-";
  }

  .footer-menu-item-list {
    max-height: 0;
    overflow: hidden;
    transition: all 0.3s ease;
  }

  .open {
    max-height: 117px;
  }

  .close {
    max-height: 0;
  }
}
</style>
