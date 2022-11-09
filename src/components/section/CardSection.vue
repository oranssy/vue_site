<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>{{ subject[0].mainTitle }}</h2>
    <p>{{ subject[0].subTitle }}</p>
    <div class="card__inner" :class="layout">
      <article class="card" v-for="card in cards" v-bind:key="card.img">
        <figure class="card__header">
          <img
            :src="require(`../../assets/img/${card.img}`)"
            :alt="card.imgAlt"
          />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{ card.title }}</h3>
          <p class="desc">{{ card.desc }}</p>
          <a class="btn" href="/">
            {{ card.more }}
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
  data: function () {
    return {
      subject: [
        {
          mainTitle: "The power of the sun",
          subTitle: "about solar power",
        },
      ],
      cards: [
        {
          img: "site01_card01.jpg",
          imgAlt: "The Solar System",
          title: "The Solar System",
          desc: "A star system is a group of planets, meteors, or other objects that orbit a large star. While there are many star systems, including at least 200 billion other stars in our galaxy, there is only one solar system. That's because our sun is known by its Latin name, Sol.",
          more: "view more",
        },
        {
          img: "site01_card02.jpg",
          imgAlt: "Solar Power",
          title: "Solar Power",
          desc: "California, a leading state in solar power, has found many ways to harness the Sun, the most powerful source of energy on the planet. Cities, such as Sacramento, are working to make solar power competitively priced and reliable with bulk use of solar cells and solar panels.",
          more: "view more",
        },
        {
          img: "site01_card03.jpg",
          imgAlt: "Solar Eclipse",
          title: "Solar Eclipse",
          desc: "A total solar eclipse only happens somewhere on Earth once every year or two. What is an eclipse? Learn more about how solar eclipses happen, the four types of eclipses, and how to view the sun safely if you're within the path of totality.",
          more: "view more",
        },
      ],
    };
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
