<template>
  <section id="imgTextType" class="imgText__wrap" :class="attr">
    <h2 class="blind">이미지텍스트 타입</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>Space Probes</span>
        <h3>Exploration</h3>
        <p>
          Human space exploration helps to address fundamental questions about
          our place in the Universe and the history of our solar system.
        </p>
        <ul>
          <li>
            <a href="/">Jan 7, 1610 CE: Galileo Discovers Jupiter’s Moons</a>
          </li>
          <li><a href="/">Apollo 11 Astronauts on Moon</a></li>
          <li><a href="/">Oct 4, 1957 CE: USSR Launches Sputnik</a></li>
          <li><a href="/">Women of NASA</a></li>
          <li><a href="/">Exploring Mars</a></li>
          <li><a href="/">scale of the universe 2</a></li>
        </ul>
      </div>
      <div class="imgText__img img1">
        <a href="/">Star Search</a>
      </div>
      <div class="imgText__img img2">
        <a href="/" class="blue">Space Gym</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>

<style>
/* 이미지 텍스트 유형 */
.imgText__inner {
  display: flex;
  justify-content: space-between;
}

.imgText__inner > div {
  width: 32%;
  height: 500px;
}

.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}

.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  word-break: keep-all;
  line-height: 1.4;
  margin-bottom: 20px;
}

.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #666;
  margin-bottom: 10px;
}

.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.6;
}

.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}

.imgText__txt li {
  color: #666;
}

.imgText__txt li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}

.imgText__img {
  border-radius: 10px;
  position: relative;
}

.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: #2c0d12;
  color: #fff;
  font-size: 18px;
  padding: 10px 30px;
  border-radius: 30px;
  display: inline-block;
}

.imgText__img a.blue {
  background-color: #0d1227;
}

.imgText__img.img1 {
  background: url(../../assets/img/site01_imgtext01.jpg) no-repeat center /
    cover;
}

.imgText__img.img2 {
  background: url(../../assets/img/site01_imgtext02.jpg) no-repeat center /
    cover;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    /* height값 초기화 */
    height: auto;
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 49%;
  }
}

@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img:first-child {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
