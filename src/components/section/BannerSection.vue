<template>
  <section id="bannerType" class="banner__wrap" :class="fonts">
    <h2 class="blind">{{ banners[0].title }}</h2>
    <div class="banner__inner">
      <h3 class="title">{{ banners[0].title }}</h3>
      <p class="desc">
        {{ banners[0].desc }}
        <a :href="banners[0].link1" :title="banners[0].linkTitle">{{
          banners[0].link2
        }}</a>
      </p>
      <span class="small">{{ banners[0].author }}</span>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    fonts: String,
  },
  data: function () {
    return {
      banners: [
        {
          title: "Black Hole",
          desc: "What is inside black hole?",
          link1: "https://youtu.be/e-P5IFTqB98",
          link2: "https://www.youtube.com/c/inanutshell",
          linkTitle: "유튜브 페이지로 이동",
          author: "Kurzgesagt - In a Nutshell",
        },
      ],
    };
  },
};
</script>

<style>
.banner__inner {
  background-image: url(../../assets/img/site01_banner01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
