<script>
import debounce from '~/assets/debounce'

export default {
  name: 'V5',

  data () {
    return {
      height: 0
    }
  },

  computed: {
    layoutStyles () {
      return { height: `${this.height}px` }
    }
  },

  mounted () {
    this.getPageDimensions()
    window.addEventListener('resize', debounce(this.getPageDimensions, 100))
  },

  methods: {
    getPageDimensions () {
      console.log(document.documentElement.clientHeight)
      this.height = document.documentElement.clientHeight
    }
  }
}
</script>

<template lang="pug">
.layout(:style="layoutStyles")
  .layout__header v5
  .layout__content body 100%, layout JS {{ height }}
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
  height 100%

body
  overflow hidden
  overscroll-behavior-y contain // disable pull to refresh
</style>

<style lang="stylus" scoped>
.layout
  display flex
  flex-flow column
  height 100%
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
