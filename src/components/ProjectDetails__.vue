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
                <a class="header__list-link" href="index.html#project-section">Домой</a>
              </li>
              <li class="header__list-item">
                <a class="header__list-link" href="projects.html">Наши успехи</a>
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
      <section class="main-project-details" id="project-details-up">
        <div class="container-blog">
          <div class="main-blog-section__content"></div>
        </div>
      </section>
      <div class="project-details__inner">
        <div class="text-content">
          <h2 class="project-details__title">Минималистичные спальни</h2>
          <span style="display: block; padding-bottom: 40px;"></span>
          <p>В своей статье от 1994-го года журнал «Before & After» отследил фразу «Lorem ipsum ...» до философского трактата Цицерона О пределах добра и зла, написанного в 45 году до нашей эры на латинском языке. В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...». Id atque molestias dolor doloremque. Natus illum quia sunt numquam voluptatem, earum molestiae labore enim, aperiam vitae placeat.</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id atque molestias dolor doloremque. Natus illum quia sunt numquam voluptatem, earum molestiae labore enim, aperiam vitae placeat quisquam! Distinctio qui assumenda repellat repellendus commodi minus ullam quisquam ipsam facilis possimus eos consectetur, a vero, maxime sit molestias quis eaque odit veritatis architecto. Ex maxime repudiandae vero asperiores reiciendis nulla fugiat ullam dolorum, eos, assumenda iure quo sed obcaecati enim. Vero voluptas tempore blanditiis eos incidunt iusto corporis ratione, vel adipisci, dignissimos, numquam dicta et officiis fuga unde fugiat deserunt debitis delectus?Id atque molestias dolor doloremque. Natus illum quia sunt numquam voluptatem, earum molestiae labore enim, aperiam vitae placeat.</p>
          <p class="project-details__description">Suscipit, animi nisi dicta explicabo aliquid nemo laboriosam, earum, ipsum! Natus illum quia sunt.</p>
        </div>
        <div class="carousel">
          <div class="carousel__inner" id="carouselInner">
            <div class="carousel__item">
              <img src="@/assets/images/project-details-1.jpg" alt="Image 1">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-2.jpg" alt="Image 2">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-3.jpg" alt="Image 3">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-4.jpg" alt="Image 4">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-5.jpg" alt="Image 5">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-6.jpg" alt="Image 6">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-7.jpg" alt="Image 7">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-8.jpg" alt="Image 8">
            </div>
            <div class="carousel__item">
              <img src="@/assets/images/project-details-9.jpg" alt="Image 9">
            </div>
          </div>
          <div class="carousel__controls">
            <button class="carousel__control" @click="prevSlide">←</button>
            <button class="carousel__control" @click="nextSlide">→</button>
          </div>
        </div>
        <div class="text-content">
          <p>В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...». </p>
          <a href="projects.html">Все Наши Проекты</a>
          <p>В своей статье от 1994-го года журнал «Before & After» отследил фразу «Lorem ipsum ...» до философского трактата Цицерона О пределах добра и зла, написанного в 45 году до нашей эры на латинском языке. В оригинале текст выглядит так «Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit ...», и переводится как «Нет никого, кто любил бы свою боль, кто искал бы ее и хотел бы чтобы она была у него. Потому что это боль...». Id atque molestias dolor doloremque. Natus illum quia sunt numquam voluptatem, earum molestiae labore enim, aperiam vitae placeat.</p>
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
              <a class="header__list-link" href="index.html#main-section">Домой</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="blog-details.html">Новости</a>
            </div>
            <br>
            <div class="header__list-item">
              <a class="header__list-link" href="blog.html">Блог</a>
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
  name: 'ProjectDetailsComponent',
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
