<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>The power of the sun</h2>
    <p>about solar power</p>
    <div class="card__inner" :class="layout">
      <article class="card">
        <figure class="card__header">
          <img
            src="../../assets/img/site01_card01.jpg"
            alt="반려견의 다양한 표정 바로알기"
          />
        </figure>
        <div class="card__body">
          <h3 class="tit">The Solar System</h3>
          <p class="desc">
            A star system is a group of planets, meteors, or other objects that
            orbit a large star. While there are many star systems, including at
            least 200 billion other stars in our galaxy, there is only one solar
            system. That's because our sun is known by its Latin name, Sol.
          </p>
          <a class="btn" href="/">
            view more
            <span>
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0L0 4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img
            src="../../assets/img/site01_card02.jpg"
            alt="반려견의 문제 행동 파악하기"
          />
        </figure>
        <div class="card__body">
          <h3 class="tit">Solar Power</h3>
          <p class="desc">
            California, a leading state in solar power, has found many ways to
            harness the Sun, the most powerful source of energy on the planet.
            Cities, such as Sacramento, are working to make solar power
            competitively priced and reliable with bulk use of solar cells and
            solar panels.
          </p>
          <a class="btn" href="/">
            view more
            <span aria-hidden="true">
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0L0 4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img
            src="../../assets/img/site01_card03.jpg"
            alt="반려견과의 놀이방법 알아보기"
          />
        </figure>
        <div class="card__body">
          <h3 class="tit">Solar Eclipse</h3>
          <p class="desc">
            A total solar eclipse only happens somewhere on Earth once every
            year or two. What is an eclipse? Learn more about how solar eclipses
            happen, the four types of eclipses, and how to view the sun safely
            if you're within the path of totality.
          </p>
          <a class="btn" href="/">
            view more
            <span>
              <svg
                width="65"
                height="8"
                viewBox="0 0 65 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0L0 4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
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
/* 카드 영역 */
.card__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.card {
  width: 32%;
  background: #f5f5f5;
}

.card__body {
  padding: 24px;
}

.card__body .tit {
  font-size: 24px;
  margin-bottom: 10px;
  overflow: hidden;
  /* 1줄 효과 */
  white-space: nowrap;
  /* 1줄 효과 */
  text-overflow: ellipsis;
  /* 1줄 효과 */
  padding-right: 20px;
  /* 글자가 짤리는 것 방지 */
}

.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}

.card__body .btn:hover {
  text-decoration: underline;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
