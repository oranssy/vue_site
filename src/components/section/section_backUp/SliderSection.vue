<template>
  <section id="sliderType" class="slider__wrap" :class="fonts">
    <h2 class="blind">슬라이드 영역</h2>
    <div class="slider__inner">
      <swiper
        :spaceBetween="30"
        :centeredSlides="true"
        :autoplay="{
          delay: 2500,
          disableOnInteraction: false,
        }"
        :pagination="{
          clickable: true,
        }"
        :navigation="true"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide>
          <div class="desc">
            <span>LIBRARY</span>
            <h3>SPACE</h3>
            <p>
              For thousands of years, people have looked up at the night sky
              with questions. <br />
              As technologies have advanced so to has our ability to investigate
              those questions.
            </p>
            <div class="btn">
              <a href="/">Learn more</a>
              <a href="/" class="black"> View resource </a>
            </div>
          </div></swiper-slide
        >
        <swiper-slide>
          <div class="desc">
            <span>LIBRARY</span>
            <h3>SPACE</h3>
            <p>
              For thousands of years, people have looked up at the night sky
              with questions. <br />
              As technologies have advanced so to has our ability to investigate
              those questions.
            </p>
            <div class="btn">
              <a href="/">Learn more</a>
              <a href="/" class="black"> View resource </a>
            </div>
          </div></swiper-slide
        >
        <swiper-slide>
          <div class="desc">
            <span>LIBRARY</span>
            <h3>SPACE</h3>
            <p>
              For thousands of years, people have looked up at the night sky
              with questions. <br />
              As technologies have advanced so to has our ability to investigate
              those questions.
            </p>
            <div class="btn">
              <a href="/">Learn more</a>
              <a href="/" class="black"> View resource </a>
            </div>
          </div></swiper-slide
        >
      </swiper>
    </div>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

import { Autoplay, Pagination, Navigation } from "swiper";

export default {
  props: {
    fonts: String,
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>

<style>
/* slider */
.slider__inner {
  /* width: 100%; */
  margin-top: 40px;
}

.slider {
  position: relative;
}

.slider__img {
  /* height: 500px; */
  background: url(../../assets/img/site01_slider01.jpg) no-repeat center / cover;
}

.slider__img .desc {
  width: 1160px;
  margin: 0 auto;
  padding: 100px 20px;
}

.slider__img .desc span {
  font-size: 16px;
  background-color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}

.slider__img .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}

.slider__img .desc p {
  font-size: 20px;
  font-weight: 300;
  color: #fff;
  line-height: 1.35;
  margin-bottom: 130px;
}

.slider__img .desc .btn a {
  font-size: 16px;
  background-color: #fff;
  padding: 11px 50px;
  display: inline-block;
  transition: all 0.3s ease;
}

.slider__img .desc .btn a.black {
  background-color: #000;
  color: #fff;
}

.slider__arrow a {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 30px;
  height: 56px;
  background-image: url(../../assets/img/slider_icon.svg);
}

.slider__arrow a.left {
  left: 20px;
}

.slider__arrow a.right {
  right: 20px;
  background-position: -50px 0;
}

.slider__dot {
  position: absolute;
  left: 50%;
  transform: translateY(-50%);
  bottom: 25px;
}

.slider__dot a {
  display: inline-block;
  width: 16px;
  height: 16px;
  background-image: url(../../assets/img/slider_icon.svg);
  background-position: -20px -70px;
}

.slider__dot a.active {
  background-position: 0px -70px;
}

.slider__dot a.play {
  background-position: -40px -70px;
}

.slider__dot a.stop {
  background-position: -60px -70px;
}

/* swiper */
.swiper-slide {
  background: url(../../assets/img/site01_slider01.jpg) no-repeat center / cover;
}

.swiper-slide:nth-child(2) {
  background: url(../../assets/img/site01_slider02.jpg) no-repeat center / cover;
}

.swiper-slide:nth-child(3) {
  background: url(../../assets/img/site01_slider03.jpg) no-repeat center / cover;
}

.swiper-slide .desc {
  width: 1160px;
  margin: 0 auto;
  padding: 100px 20px;
  box-sizing: border-box;
}

.swiper-slide .desc span {
  font-size: 16px;
  background-color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}

.swiper-slide .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}

.swiper-slide .desc p {
  font-size: 20px;
  font-weight: 300;
  color: #fff;
  line-height: 1.35;
  margin-bottom: 130px;
}

.swiper-slide .desc .btn a {
  font-size: 16px;
  background-color: #fff;
  padding: 11px 50px;
  display: inline-block;
  transition: all 0.3s ease;
}

.swiper-slide .desc .btn a.black {
  background-color: #000;
  color: #fff;
}

.swiper-slide .desc .btn a:hover {
  border-radius: 50px;
}

.swiper-button-next {
  background-position: -50px 0;
}

.swiper-button-next,
.swiper-button-prev {
  width: 30px !important;
  height: 56px !important;
  background-image: url(../../assets/img/slider_icon.svg);
}

.swiper-button-next {
  background-position: -50px 0;
}

.swiper-button-next::after,
.swiper-button-prev::after {
  opacity: 0;
}

.swiper-pagination-bullet {
  width: 16px !important;
  height: 16px !important;
  background-image: url(../../assets/img/slider_icon.svg) !important;
  background-position: -20px -70px !important;
  background-color: transparent !important;
  opacity: 1 !important;
}

.swiper-pagination-bullet-active {
  background-position: 0px -70px !important;
}

.swiper-button {
  position: absolute;
  left: 50%;
  margin-left: 40px;
  bottom: 25px;
  z-index: 1000;
  display: flex;
}

.swiper-button-stop {
  background-image: url(../../assets/img/slider_icon.svg) !important;
  background-position: -60px -70px;
  width: 16px;
  height: 16px;
  cursor: pointer;
}

.swiper-button-play {
  background-image: url(../../assets/img/slider_icon.svg) !important;
  background-position: -40px -70px;
  width: 16px;
  height: 16px;
  cursor: pointer;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .swiper-slide .desc {
    width: 100%;
    text-align: center;
  }
  .swiper-slide .desc h3 {
    font-size: 70px;
  }
}

@media (max-width: 600px) {
  .swiper-slide .desc {
    padding: 80px 0;
  }
  .swiper-slide .desc h3 {
    font-size: 40px;
  }
  .swiper-slide .desc p {
    font-size: 16px;
    margin-bottom: 50px;
  }
  .swiper-slide .desc .btn a {
    padding: 10px 25px;
  }
}
</style>
