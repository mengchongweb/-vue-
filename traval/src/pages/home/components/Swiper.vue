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
          imgUrl: 'https://s1.veryins.com/image/v/t51.2885-15/sh0.08/e35/c0.156.1249.1249a/s640x640/122850755_1097654547304449_2010801854177486625_n.jpg?_nc_ht=scontent-nrt1-1.cdninstagram.com&_nc_cat=109&_nc_ohc=7Traa9rQdagAX95V5XU&oh=9cb8100fd6a60775db8004b0b3636291&oe=5FC208C5'
        },
        {
          id: '1',
          imgUrl: 'https://s3.veryins.com/image/v/t51.2885-15/sh0.08/e35/c0.180.1440.1440a/s640x640/122812327_1004144540087921_6904608624888708573_n.jpg?_nc_ht=scontent-nrt1-1.cdninstagram.com&_nc_cat=105&_nc_ohc=JkJ3fAvxfjoAX-Htuxt&oh=ce5a8c5be84fb8319b79ba2c46c2a03a&oe=5FC0C3A1'
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
