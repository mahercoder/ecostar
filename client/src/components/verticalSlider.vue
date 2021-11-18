<template>
  <div class="swiper_slider">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <img src="../assets/2.jpg" alt="" />
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/1.png" alt="" />
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/2.png" alt="" />
      </swiper-slide>
      <swiper-slide>
        <img src="../assets/3.png" alt="" />
      </swiper-slide>
      <div
        class="swiper-pagination swiper-pagination-bullets"
        slot="pagination"
      ></div>
      <div class="swiper-button-prev" slot="button-prev">
        <img src="../assets/arrowt.svg" alt="">
      </div>
    <div class="swiper-button-next" slot="button-next">
        <img src="../assets/arrowb.svg" alt="">
    </div>
    </swiper>
  </div>
</template>

<script>
import SwiperCore, { Pagination, Autoplay, Navigation } from "swiper";
SwiperCore.use([Pagination, Autoplay, Navigation]);
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.min.css";

export default {
  name: "swiper-example-vertical",
  title: "Vertical slider",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiperOption: {
        slidesPerView: 2,
        spaceBetween: 50,
        autoplay: true,
        centeredSlides: true,
        loop:true,
        direction: "vertical",
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
          renderBullet(index, className) {
            return `<span class="${className} swiper-pagination-bullet-custom">0${index +
              1}</span>`;
          },
        },
      },
    };
  },
  mounted() {
    const header = document.querySelector(".header_title");
    console.log(header);
  },
};
</script>

<style lang="scss">
// @import './base.scss'; 
.swiper {
  max-height: 650px;
}
.swiper-slide {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  img {
    max-width: 100%;
    height: 100%;
  }
}
.swiper-button-next:after, .swiper-button-prev:after{
  display: none;
}
.swiper-button-next{
  left: 20px !important;
  right: auto !important;
 
  bottom: 25% !important;
  top:auto !important;
}
.swiper-button-prev{
  left: 20px !important;
  right: auto !important;
   top:25% !important;
  bottom:auto !important;
}
.swiper-container-vertical > .swiper-pagination-bullets {
  left: 10px !important;
  right: calc(100%-10px) !important;
}
.swiper-pagination-bullet {
  width: 40px !important;
  height: 40px !important;
  box-sizing: border-box;
  border-radius: 6px;
  background: transparent;
  display: flex !important;
  justify-content: center;
  align-items: center;
  color: #5f5f5f !important;
  opacity: 1 !important;
  transition: 0.5s !important;
  margin-bottom: 30px !important;
  &-active {
    background: transparent;
    border: 1px solid #000000;
    color: #000 !important;
  }
}
</style>
