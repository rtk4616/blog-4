<template>
  <button type="button" class="navbar-toggle collapsed" @click="toggle">
    <span class="sr-only">Toggle navigation</span>
    <span class="icon-bar"></span>
    <span class="icon-bar"></span>
    <span class="icon-bar"></span>
  </button>
</template>

<script>
  import types from '../../store/mutationTypes'

  export default {
    methods: {
      toggle () {
        this.$store.commit(types.TOGGLE_ASIDE)
      }
    }
  }
</script>

<style lang="less" rel="stylesheet/less" scoped>
  @import "./../../assets/css/variables";

  .navbar-toggle {
    background: #000;
    opacity: .25;
    display: none;
    z-index: 1000;
    position: fixed;
    top: 15px;
    right: 15px;
    margin: 0;

    .icon-bar {
      background-color: #fff;
    }

    @media (max-width: @screen-xs-max) {
      display: block;
    }

    @media print {
      display: none;
    }
  }
</style>
