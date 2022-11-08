<template>
  <footer id="footerType" class="footer__wrap" :class="attr">
    <h2 class="blind">footer</h2>
    <div class="footer__inner" :class="attr">
      <div class="footer__menu">
        <div>
          <h3>About</h3>
          <ul>
            <li>
              <a href="/">News and Impact</a>
            </li>
            <li>
              <a href="/">Contact</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>Learn</h3>
          <ul>
            <li>
              <a href="/">Introduction</a>
            </li>
            <li>
              <a href="/">Features</a>
            </li>
            <li>
              <a href="/">FAQ</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>Explore</h3>
          <ul>
            <li>
              <a href="/">Our Explorers</a>
            </li>
            <li>
              <a href="/">Our Projects</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>Participate</h3>
          <ul>
            <li>
              <a href="/">Community</a>
            </li>
            <li>
              <a href="/">Contributors</a>
            </li>
            <li>
              <a href="/">Events</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>Resources</h3>
          <ul>
            <li>
              <a href="/">About</a>
            </li>
            <li>
              <a href="/">Design</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>JOIN US</h3>
          <ul>
            <li>
              <a href="/">Ways to Give</a>
            </li>
            <li>
              <a href="/">Apply for a Grant</a>
            </li>
            <li>
              <a href="/">Careers</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        2022 oranssy. portfolio is here.
        <br />
        All rights reserved.
      </div>
    </div>
  </footer>
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
.footer__inner {
  width: 85%;
  padding: 0 20px;
  margin: 0 auto;
}

.footer__menu {
  display: flex;
  justify-content: space-between;
  margin-bottom: 70px;
}

.footer__menu h3 {
  font-size: 18px;
  margin-bottom: 20px;
}

.footer__menu li {
  list-style: none;
}

.footer__menu li a {
  font-size: 14px;
  color: #666;
  margin-bottom: 10px;
  display: block;
}

.footer__right {
  border-top: 1px solid #d9d9d9;
  text-align: center;
  padding-top: 40px;
  color: #666;
  line-height: 1.5;
}

/* 미디어쿼리 */
@media (max-width: 960px) {
  .footer__menu {
    display: none;
  }

  .footer__right {
    padding-top: 0;
    margin-top: 0;
  }

  .footer__wrap {
    padding: 40px 0;
  }
}
</style>
