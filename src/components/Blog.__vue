<template>
  <div class="wrapper">
    <header class="header" id="blog-section">
      <div class="container">
        <div class="header__inner">
          <picture>
            <img class="header__logo" src="@/assets/images/logo.png" alt="">
          </picture>
          <nav class="header__nav">
            <ul class="header__nav-list header__list">
              <li class="header__list-item">
                <a class="header__list-link" href="projects.html">Проекты</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="blog-details.html">Наши успехи</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="index.html">Домой</a>
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
      <section class="main-blog-section" id="blog-up">
        <div class="container-blog">
          <div class="main-blog-section__content">
            <h1 class="main-blog-section__title">Статьи & Новости</h1>
          </div>
        </div>
        <div class="blog__inner">
          <div class="blogs__box-up">
            <div class="blog__box-up">
              <div class="blog__box-content">
                <picture>
                  <img class="blog__box-img-top" src="@/assets/images/blog-top.png" alt="">
                </picture>
                <div class="blog__box-details">
                  <h4 class="blog__box-title">Low Cost Latest Invented Interior Designing Ideas</h4>
                  <p class="blog__box-text">С того времени этот, похожий на латинский, текст стал стандартом в печатной
                    промышленности для примеров шрифтов и текстов. Перед появлением электронных издательств дизайнеры
                    импровизировали в работе над макетами, изображая текст при помощи волнистых линий. С появлением
                    самоклеющихся наклеек с напечатанным текстом «Lorem ipsum» появился более реалистичный способ
                    обозначения расположения текста на странице.</p>
                  <div class="blog__box-bottom">
                    <time datetime="2021-11-23" class="blog__box-date">26 Декабря, 2024</time>
                    <a class="blog__box-btn" href="blog-details.html"></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="blogs" id="blog-up-section">
        <div class="container">
          <h2 class="blogs__title">Статьи & Новости</h2>
          <p class="blogs__title-text">Хорошо известно, что читатель будет отвлекаться</p>
          <div class="blogs__inner">
            <div class="blogs__box" v-for="blog in blogs" :key="blog.id">
              <div class="blogs__box-top">
                <picture>
                  <img class="blogs__box-img" :src="blog.image" :alt="blog.title">
                </picture>
                <span class="blogs__box-details">{{ blog.category }}</span>
              </div>
              <h4 class="blogs__box-title">{{ blog.title }}</h4>
              <div class="blogs__box-bottom">
                <time :datetime="blog.date" class="blogs__box-date">{{ blog.dateFormatted }}</time>
                <a class="blogs__box-btn" :href="blog.link"></a>
              </div>
            </div>
          </div>
        </div>
      </section>
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
              <a class="header__list-link" href="index.html#main-section">Домой</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="projects.html#project-section">Проекты</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="blog.html#blog-section">Блог</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="index.html#achievements">Наши успехи</a>
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
  name: 'BlogComponent',
  data() {
    return {
      blogs: [
        {
          id: 1,
          image: require('@/assets/images/blog-1.jpg'),
          category: 'Дизайн Кухни',
          title: 'Создадим лучший макет перепланировки',
          date: '2021-11-23',
          dateFormatted: '26 Декабря, 2024',
          link: 'blog-details.html'
        },
        {
          id: 2,
          image: require('@/assets/images/blog-2.jpg'),
          category: 'Дизайн для Жизни',
          title: 'Лучшие интерьерные идеи по низкой цене',
          date: '2021-11-23',
          dateFormatted: '22 Декабря, 2024',
          link: 'blog-details.html'
        },
        {
          id: 3,
          image: require('@/assets/images/blog-3.jpg'),
          category: 'Дизайн Интерьера',
          title: 'Лучшие интерьерные решения для офисов',
          date: '2021-11-23',
          dateFormatted: '25 Декабря, 2024',
          link: 'blog-details.html'
        }
      ]
    };
  }
};
</script>

<style scoped>
/* Add "scoped" attribute to limit CSS to this component only */
@import '@/assets/css/main.css';
@import '@/assets/css/media.css';
@import '@/assets/css/normalise.css';
</style>
