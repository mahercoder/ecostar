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
        class="swiper-pagination swiper-pagination-bullets bullets"
        slot="pagination"
      ></div>
      <div class="swiper-button-prev prev" slot="button-prev">
        <img src="../assets/arrowt.svg" alt="">
      </div>
    <div class="swiper-button-next next" slot="button-next">
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
        slidesPerView: 3,
        spaceBetween: 50,
        autoplay: true,
        centeredSlides: true,
        loop: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
          renderBullet(index, className) {
            return `<span class="${className} swiper-pagination-bullet-custom">0${index +
              1}</span>`;
          },
        },
        breakpoints: {
            1024: {
              slidesPerView: 3,
              spaceBetween: 40
            },
            768: {
              slidesPerView: 3,
              spaceBetween: 30
            },
            640: {
              slidesPerView: 2,
              spaceBetween: 20
            },
            320: {
              slidesPerView: 1,
              spaceBetween: 10
            }
          }
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
  padding-bottom: 50px;
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
.swiper-button-next:after,
.swiper-button-prev:after {
  display: none;
}
.next {
  left: auto !important;
  right: 20px !important;
  bottom: 0px !important;
  top: auto !important;
  transform: rotate(-90deg);
}
.prev {
  left: 20px !important;
  right: auto !important;
  top: auto !important;
  bottom: 0px !important;
  transform: rotate(-90deg);
}
.bullets {
  left: 50% !important;
  transform: translateX(-50%);
  bottom: -25px !important;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bullets .swiper-pagination-bullet {
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
