<script>
export default {
  name: 'V4'
}
</script>

<template lang="pug">
.layout
  .layout__header v4
  .layout__content body 100vh, layout 100vh
  .layout__bottom bottom
</template>

<style lang="stylus">
*
  box-sizing border-box
  -webkit-tap-highlight-color transparent
  margin 0
  border 0

  &:focus
    outline 0

strong
  font-weight bold

html
body
#__nuxt
#__layout
  height 100vh

body
  overflow hidden
  overscroll-behavior-y contain // disable pull to refresh
</style>

<style lang="stylus" scoped>
.layout
  display flex
  flex-flow column
  height 100vh
  align-items center
  justify-content space-between
  color white

  &__header
    background red

  &__content
    background blue

  &__bottom
    background purple
</style>
