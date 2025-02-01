<template>
  <div class="wrapper">
    <header class="header" id="main-section">
      <div class="container">
        <div class="header__inner">
          <picture>
            <img class="header__logo" src="@/assets/images/logo.png" alt="">
          </picture>
          <nav class="header__nav">
            <ul class="header__nav-list header__list">
              <li class="header__list-item">
                <a class="header__list-link" href="#project-section">Проекты</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="#achievements">Наши успехи</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="blog.html">Блог</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="#contact-section">Контакты</a>
              </li>
            </ul>
            <div class="icon-menu">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </nav>
          <div class="header__plate"></div>
        </div>
      </div>
    </header>
    <main class="main">
      <section class="main-section">
        <div class="container">
          <div class="main-section__content">
            <h1 class="main-section__title">Пусть<br> ваш дом будет уникальным</h1>
            <p class="main-section__title-text">Существует много вариаций Lorem Ipsum,
              <br> которые можно использовать.
            </p>
            <a class="main-section__btn" href="projects.html">Начать</a>
          </div>
        </div>
      </section>
      <section class="projects" id="project-section">
        <div class="container">
          <h2 class="projects__title">Следите за нашими проектами</h2>
          <p class="projects__title-text">С инструментами, облегчающими процесс, и поддержкой команды профессионалов
            <br> начать работать с нами проще простого.
          </p>
          <div class="projects__items">
            <div class="projects__item">
              <div class="project__item-top">
                <picture>
                  <img class="project__item-img" src="@/assets/images/project-1.png" alt="">
                </picture>
              </div>
              <div class="project__item-bottom">
                <div class="project__item-info project-info">
                  <h4 class="project-info__name">Современная кухня</h4>
                  <span class="project-info__style">Декор / Планировка</span>
                </div>
                <a href="projects.html" class="project__item-btn"></a>
              </div>
            </div>
            <div class="projects__item">
              <div class="project__item-top">
                <picture>
                  <img class="project__item-img" src="@/assets/images/project-2.png" alt="">
                </picture>
              </div>
              <div class="project__item-bottom">
                <div class="project__item-info project-info">
                  <h4 class="project-info__name">Современная кухня</h4>
                  <span class="project-info__style">Декор / Планировка</span>
                </div>
                <a href="projects.html" class="project__item-btn"></a>
              </div>
            </div>
            <div class="projects__item">
              <div class="project__item-top">
                <picture>
                  <img class="project__item-img" src="@/assets/images/project-3.png" alt="">
                </picture>
              </div>
              <div class="project__item-bottom">
                <div class="project__item-info project-info">
                  <h4 class="project-info__name">Современная кухня</h4>
                  <span class="project-info__style">Декор / Планировка</span>
                </div>
                <a href="projects.html" class="project__item-btn"></a>
              </div>
            </div>
            <div class="projects__item">
              <div class="project__item-top">
                <picture>
                  <img class="project__item-img" src="@/assets/images/project-4.png" alt="">
                </picture>
              </div>
              <div class="project__item-bottom">
                <div class="project__item-info project-info">
                  <h4 class="project-info__name">Современная кухня</h4>
                  <span class="project-info__style">Декор / Планировка</span>
                </div>
                <a href="projects.html" class="project__item-btn"></a>
              </div>
            </div>
          </div>
        </div>
      </section>
      <div class="achievements" id="achievements">
        <div class="container">
          <div class="achievements__inner">
            <div class="achievements__box">
              <div class="achievements__number">12</div>
              <span class="achievements__text">Лет Опыта</span>
            </div>
            <div class="achievements__box">
              <div class="achievements__number">85</div>
              <span class="achievements__text">Успешных Проектов</span>
            </div>
            <div class="achievements__box">
              <div class="achievements__number">15</div>
              <span class="achievements__text">Проектов в Работе</span>
            </div>
            <div class="achievements__box">
              <div class="achievements__number">95</div>
              <span class="achievements__text">Счастливых Клиентов</span>
            </div>
          </div>
        </div>
      </div>
    </main>
    <footer class="footer" id="contact-section">
      <div class="container">
        <div class="footer__inner">
          <div class="footer__logo">
            <picture>
              <img class="footer__logo-img" src="@/assets/images/logo.png" alt="">
            </picture>
            <br>
            <br>
            <br>
            <p class="footer__logo-text"></p>
            <div class="header__list-item">
              <a class="header__list-link" href="#main-section">Домой</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="#project-section">Проекты</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="blog.html">Блог</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="#achievements">Наши успехи</a>
            </div>
          </div>
          <ul class="footer__social">
            <li class="footer__social-item">
              <a class="footer__social-link" href="#">
                <picture>
                  <img class="footer__social-link-img" src="@/assets/images/tw.png" alt="">
                </picture>
              </a>
            </li>
            <li class="footer__social-item">
              <a class="footer__social-link" href="#">
                <picture>
                  <img class="footer__social-link-img" src="@/assets/images/li.png" alt="">
                </picture>
              </a>
            </li>
            <li class="footer__social-item">
              <a class="footer__social-link" href="#">
                <picture>
                  <img class="footer__social-link-img" src="@/assets/images/tw.png" alt="">
                </picture>
              </a>
            </li>
            <li class="footer__social-item">
              <a class="footer__social-link" href="#">
                <picture>
                  <img class="footer__social-link-img" src="@/assets/images/li.png" alt="">
                </picture>
              </a>
            </li>
            <li class="footer__social-item">
              <a class="footer__social-link" href="#">
                <picture>
                  <img class="footer__social-link-img" src="@/assets/images/tw.png" alt="">
                </picture>
              </a>
            </li>
          </ul>
          <div class="footer__contacts">
            <h4 class="footer__contacts-title">Контакты</h4>
            <br>
            <br>
            <p class="footer__contacts-address">55 East Birchwood Ave. Brooklyn, New York 11201</p>
            <a class="footer__contacts-email" href="mailto:contact@interno.com">contact@interno.com</a>
            <a href="tel:1234567890" class="footer__contacs-phone">(123) 456 - 7890</a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'HomeComponent',
  data() {
    return {
      currentIndex: 0
    };
  },
  methods: {
    showSlide(index) {
      const offset = -index * 100 + '%';
      document.getElementById('carouselInner').style.transform = 'translateX(' + offset + ')';
    },
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.totalItems;
      this.showSlide(this.currentIndex);
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.totalItems) % this.totalItems;
      this.showSlide(this.currentIndex);
    }
  },
  mounted() {
    this.items = document.querySelectorAll('.carousel__item');
    this.totalItems = this.items.length;
    this.showSlide(this.currentIndex);
  }
};
</script>

<style scoped>
/* Add "scoped" attribute to limit CSS to this component only */
@import '@/assets/css/main.css';
@import '@/assets/css/media.css';
@import '@/assets/css/normalise.css';
</style>
