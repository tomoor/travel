<template>
  <div class="wraper">
    <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.key">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: "HomeSwiper",
    data () {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop:true
        },
        swiperList: [{
          id: '0001',
          imgUrl:'https://p2-q.mafengwo.net/s12/M00/0E/87/wKgED1w_TeK' +
            'AcfyiAAghC45qhrI62.jpeg?imageMogr2%2Fthumbnail%2F%21750x4' +
            '22r%2Fgravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90'
        },{
          id: '0002',
          imgUrl:'https://b4-q.mafengwo.net/s12/M00/0D/AB/wKgED1w_TaaAE' +
            'AVSAAacfZZM5l890.jpeg?imageMogr2%2Fthumbnail%2F%21750x422r' +
            '%2Fgravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90'
        },{
          id: '0003',
          imgUrl:'https://b2-q.mafengwo.net/s12/M00/B6/BD/wKgED1xALdiAUMq' +
            'FAAXdW7D8e-w11.jpeg?imageMogr2%2Fthumbnail%2F%21750x422r%2Fg' +
            'ravity%2FCenter%2Fcrop%2F%21750x422%2Fquality%2F90'
        }]
      }
    }
  }
</script>

<style scoped lang="stylus">
  .wraper >>> .swiper-pagination-bullet-active
    background: #eeecf3
  .wraper
    overflow hidden
    width: 100%
    height: 0
    padding-bottom: 56%
    background: #dbdbdb
    .swiper-img
      width:100%

</style>
