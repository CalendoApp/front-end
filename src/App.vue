<template>
  <div id="app" class="wrap">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="sass">
  @import "assets/style/main"

  .wrap
    padding-top: 55px
</style>
