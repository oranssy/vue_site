<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2 class="blind">Observation</h2>
    <p>What tools are used to observe space?</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="tit white">Hubble Space Telescope</h3>
        <p class="desc white">
          It was not the first space telescope, but it is one of the largest and
          most versatile, renowned both as a vital research tool and as a public
          relations boon for astronomy.
        </p>
        <a
          class="btn"
          href="https://medium.com/life-on-the-other-planets-whats-new/nasas-hubble-telescope-is-back-online-a7e3686d607a"
          title="자세히보기"
          >view more</a
        >
      </article>
      <article class="image img2">
        <h3 class="tit white">James Webb Space Telescope</h3>
        <p class="desc white">
          This is expected to enable a broad range of investigations across the
          fields of astronomy and cosmology, such as observation of the first
          stars and the formation of the first galaxies, and detailed
          atmospheric characterization of potentially habitable exoplanets.
        </p>
        <a
          class="btn"
          href="https://www.quantamagazine.org/why-nasas-james-webb-space-telescope-matters-so-much-20211203/"
          title="자세히보기"
          >view more</a
        >
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
/* 이미지 영역 */
.image__inner {
  display: flex;
  justify-content: space-between;
}

.image {
  width: 49%;
  height: 370px;
  padding: 197px 30px 30px 30px;
  box-sizing: border-box;
}

.image.img1 {
  background: url(../../assets/img/site01_img01.jpg) no-repeat center / cover;
}

.image.img2 {
  background: url(../../assets/img/site01_img02.jpg) no-repeat center / cover;
}

.image .tit {
  font-size: 32px;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.image .tit.white {
  color: #fff;
}

.image .desc {
  font-size: 16px;
  font-weight: 400;
  line-height: 1.5;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  margin-bottom: 10px;
}

.image .desc.white {
  color: #fff;
}

.image .btn {
  font-size: 16px;
  color: #fff;
  background: #220416;
  padding: 10px 20px;
  display: inline-block;
}

@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }

  .image {
    width: 100%;
    padding: 210px 20px 20px 20px;
  }

  .image:first-child {
    margin-bottom: 20px;
  }

  .image .tit {
    font-size: 24px;
  }

  .image .desc {
    font-size: 16px;
  }
}
</style>
