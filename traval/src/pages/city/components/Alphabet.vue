<template>
  <ul class="list">
    <li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>
  </ul>
</template>

<script>
export default {
  props: {
    cities: Object
  },
  name: 'CityAlphaber',
  data () {
    return {

    }
  },
  components: {

  },
  methods: {

  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles'
  .list
    display flex
    flex-direction column
    justify-content center
    position absolute
    top 1.58rem
    right 0
    bottom 0
    width 0.4rem
    .item
      line-height 0.4rem
      text-align center
      color $bgColor
</style>
