<template>
  <nav class="navbar">
    <ul class="menu">
      <li>what's new</li>
      <li>brands</li>
      <li>curations</li>
      <li>art</li>
      <li>beauty</li>
      <li>self care</li>
      <li>style</li>
      <li>lifestyle</li>
      <li>tech</li>
      <li>stories</li>
    </ul>
  </nav>
</template>

<script lang="ts">
import {Vue, Component} from "vue-property-decorator";

@Component
export default class Navbar extends Vue {
}
</script>

<style lang="scss" scoped>
.navbar {
  font-family: "TradeBold", sans-serif;
  padding-bottom: 0;
  margin: 15px 0 0 0;
  transition: ease-in-out opacity 0.45s;
  opacity: 1;
}

.menu {
  list-style: none;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-direction: row;

  li {
    text-transform: uppercase;
    margin-right: 30px;
    font-size: 11px;
    color: #000000;
    font-weight: bold;
    font-family: "Trade Gothic LT Std", sans-serif;
    text-align: center;
  }
}

@media (max-width: 1024px) {
  .menu {
    display: none;
  }

  .navbar {
    opacity: 0;
  }
}
</style>
