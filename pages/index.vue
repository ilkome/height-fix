<script>
export default {
  name: 'IndexPage'
}
</script>

<template lang="pug">
ul
  li
    n-link(to="/v1") body 100%, layout 100vh
  li
    n-link(to="/v2") variant 2
  li
    n-link(to="/v3") variant 3
  li
    n-link(to="/v4") variant 4
</template>

<style lang="stylus" scoped>
//
</style>
