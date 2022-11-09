<template>
  <section id="textType" class="text__wrap" :class="attr">
    <h2>The Solar System</h2>
    <p>Planets</p>
    <div class="text__inner" :class="layout">
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Sun" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Sun</h3>
          <p class="desc">
            The sun keeps the planets in its orbit with a tremendous
            gravitational force. What would happen if it disappeared entirely?
            Learn about the star at the center of our solar system, and how it
            is critical to all life as we know it.
          </p>
          <a href="#">more</a>
        </div>
      </article>
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Mercury" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Mercury</h3>
          <p class="desc">
            The planet Mercury is named after the messenger of the Roman gods
            because of its fleeting nature across the sky. Find out the reason
            behind its incredible speed, if it is indeed the hottest planet in
            the Solar System, and why the smallest planet in the solar system is
            slowly shrinking.
          </p>
          <a href="#">more</a>
        </div>
      </article>
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Venus" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Venus</h3>
          <p class="desc">
            Named after the ancient Roman goddess of beauty, Venus is known for
            its exceptional brightness. Find out about the volcanoes that dot
            Venus's surface, the storms that rage in its atmosphere, and the
            surprising feature that makes Venus outshine every planet or star in
            the night sky.
          </p>
          <a href="#">more</a>
        </div>
      </article>
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Earth" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Earth</h3>
          <p class="desc">
            Earth is the only planet known to maintain life. Find out the
            origins of our home planet and some of the key ingredients that help
            make this blue speck in space a unique global ecosystem.
          </p>
          <a href="#">more</a>
        </div>
      </article>
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Mars" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Mars</h3>
          <p class="desc">
            Mars, the fourth planet from the sun, has been a source of intrigue
            throughout human history. Recent NASA exploratory expeditions
            revealed some of the planet's biggest mysteries. This video explains
            what makes Mars so different from Earth and what would happen if
            humans lived there.
          </p>
          <a href="#">more</a>
        </div>
      </article>
      <article class="text">
        <figure class="text__header">
          <img src="../../assets/img/site01_card01.jpg" alt="Jupiter" />
        </figure>
        <div class="text__box">
          <h3 class="tit">Jupiter</h3>
          <p class="desc">
            Jupiter is the oldest and most massive world in the solar system.
            Learn about the planet's origin story, its Great Red Spot and
            oceanic moons, and how this ancient world influenced the formation
            of the solar system's other planets.
          </p>
          <a href="#">more</a>
        </div>
      </article>
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
/* 텍스트 영역 */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}

.text:hover {
  background: #f5f5f5;
}

.text__title {
  font-family: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}

.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  background: url(../../assets/img/text_icon.svg);
}

.text.t1 .text__title::before {
  background-position: 0 0;
}

.text.t2 .text__title::before {
  background-position: -60px 0;
}

.text.t3 .text__title::before {
  background-position: -120px 0;
}

.text.t4 .text__title::before {
  background-position: -180px 0;
}

.text.t5 .text__title::before {
  background-position: -240px 0;
}

.text.t6 .text__title::before {
  background-position: -300px 0;
}

.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3; /* clamp 줄바꿈 3줄 이상 되면 ... 으로 바뀜 - '3줄 효과' 검색해서 사용 */
  -webkit-box-orient: vertical;
}

.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}

@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}

@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }

  .text__desc {
    font-size: 16px;
  }
}

@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
