<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img
          class="swiper-img"
          :src="item.imgUrl"
          alt=""
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      },
      swiperList: [
        {
          id: '0',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1802/e3/62ce7362ca051d02.jpg_640x200_6db551b7.jpg'
        },
        {
          id: '1',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1801/93/ce59d182aca07102.jpg_640x200_ba03d44c.jpg'
        }
      ]
    }
  },
  methods: {},
  components: {}
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  overflow
  height: 0
  width: 100%
  padding-bottom: 2%
  .swiper-img
    width: 100%
    height: 2.25rem
</style>
