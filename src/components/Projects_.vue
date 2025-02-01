<template>
  <div class="wrapper" id="app">
    <Header :navLinks="navLinks" />
    <main class="main" style="margin-bottom: 150px;">
      <section class="main-projects-section" id="blog-up">
        <div class="container-blog">
          <div class="main-blog-section__content">
            <h1 class="main-blog-section__title">Наши Проекты & работы</h1>
          </div>
          <p class="project-details__description">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab deserunt,
            nulla obcaecati. Exercitationem animi ratione, error, accusamus aspernatur officia, unde ea odit aperiam
            nobis molestiae dolorum voluptatum voluptate iusto vel nulla nisi vero.</p>
          <span style="display: block; padding-bottom: 40px;"></span>
        </div>
        <div class="projects-menu">
          <div class="projects-menu__buttons">
            <button class="smooth-button" @click="filterProjects('Кухня')">Кухня</button>
            <button class="smooth-button" @click="filterProjects('Спальня')">Спальня</button>
            <button class="smooth-button" @click="filterProjects('Гостинная')">Гостинная</button>
            <button class="smooth-button" @click="filterProjects('Прихожая')">Прихожая</button>
            <button class="smooth-button" @click="filterProjects('Балкон')">Балкон</button>
            <button class="smooth-button" @click="filterProjects('Ванная')">Ванная</button>
            <button class="smooth-button" @click="filterProjects('')">Все Проекты</button>
            <div class="border-line"></div>
          </div>
        </div>
      </section>
      <div class="projects__inner">
        <div class="projects__column">
          <div v-for="(project) in filteredProjects" :key="project.id" class="projects__item">
            <img :src="project.image" alt="project image" class="projects__img">
            <div class="projects__content">
              <div class="projects__description-wrapper">
                <h2 class="blogs__box-title">{{ project.title }}</h2>
                <a href="project-details.html" class="projects__box-btn"></a>
              </div>
              <p class="projects__description">{{ project.tag }}</p>
            </div>
          </div>
        </div>
        <div class="projects__column">
          <div v-for="(project) in filteredProjects" :key="project.id" class="projects__item">
            <img :src="project.image" alt="project image" class="projects__img">
            <div class="projects__content">
              <div class="projects__description-wrapper">
                <h2 class="blogs__box-title">{{ project.title }}</h2>
                <a href="project-details.html" class="projects__box-btn"></a>
              </div>
              <p class="projects__description">{{ project.tag }}</p>
            </div>
          </div>
        </div>
      </div>
    </main>
    <Footer :footerLinks="footerLinks" />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'ProjectsComponent',
  components: {
    Header,
    Footer
  },
  data() {
    return {
      navLinks: [
        { text: 'Домой', href: 'index.html#project-section' },
        { text: 'Наши успехи', href: 'projects.html' },
        { text: 'Блог', href: 'blog.html' },
        { text: 'Контакты', href: '#contact-section' }
      ],
      footerLinks: [
        { text: 'Домой', href: 'index.html' },
        { text: 'Новости', href: 'blog-details.html' },
        { text: 'Блог', href: 'blog.html' },
        { text: 'Наши успехи', href: 'index.html#achievements' }
      ],
      projects: [
        { id: 1, image: require('@/assets/images/project-1.jpg'), title: 'Минималистичная гостинная 1', tag: 'Гостинная' },
        { id: 2, image: require('@/assets/images/project-2.jpg'), title: 'Минималистичная спальня 1', tag: 'Спальня' },
        { id: 3, image: require('@/assets/images/project-17.jpg'), title: 'Минималистичный балкон 2', tag: 'Балкон' },
        { id: 4, image: require('@/assets/images/project-12.jpg'), title: 'Минималистичная прихожая 1', tag: 'Прихожая' },
        { id: 5, image: require('@/assets/images/project-14.jpg'), title: 'Минималистичная ванная 1', tag: 'Ванная' },
        { id: 6, image: require('@/assets/images/project-16.jpg'), title: 'Минималистичный балкон 1', tag: 'Балкон' },
        { id: 7, image: require('@/assets/images/project-8.jpg'), title: 'Минималистичная гостинная 2', tag: 'Гостинная' },
        { id: 8, image: require('@/assets/images/project-7.jpg'), title: 'Минималистичная гостинная 3', tag: 'Гостинная' },
        { id: 9, image: require('@/assets/images/project-19.jpg'), title: 'Минималистичная кухня 1', tag: 'Кухня' },
        { id: 10, image: require('@/assets/images/project-10.jpg'), title: 'Минималистичная прихожая 8', tag: 'Прихожая' },
        { id: 11, image: require('@/assets/images/project-11.jpg'), title: 'Минималистичная прихожая 9', tag: 'Прихожая' },
        { id: 12, image: require('@/assets/images/project-22.jpg'), title: 'Минималистичная кухня 14', tag: 'Кухня' },
        { id: 13, image: require('@/assets/images/project-9.jpg'), title: 'Минималистичная спальня 15', tag: 'Спальня' },
        { id: 14, image: require('@/assets/images/project-21.jpg'), title: 'Минималистичная кухня 9', tag: 'Кухня' },
        { id: 15, image: require('@/assets/images/project-13.jpg'), title: 'Минималистичная ванная 2', tag: 'Ванная' },
        { id: 16, image: require('@/assets/images/project-23.jpg'), title: 'Минималистичная ванная 3', tag: 'Ванная' }
      ],
      selectedTag: ''
    };
  },
  computed: {
    filteredProjects() {
      if (this.selectedTag) {
        return this.projects.filter(project => project.tag === this.selectedTag);
      }
      return this.projects;
    }
  },
  methods: {
    filterProjects(tag) {
      this.selectedTag = tag;
    },
    setupButtonListeners() {
      const buttons = this.$el.querySelectorAll('.projects-menu__buttons button');
      const borderLine = this.$el.querySelector('.border-line');
      borderLine.style.transform = `translateX(${buttons.length - 1}00%)`;
      buttons.forEach((button, index) => {
        button.addEventListener('click', () => {
          borderLine.style.transform = `translateX(${index * 100}%)`;
        });
      });
    },
    setupSmoothScroll() {
      this.$el.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
          e.preventDefault();
          document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
          });
        });
      });
    }
  },
  mounted() {
    this.setupButtonListeners();
    this.setupSmoothScroll();
  }
};
</script>

<style scoped>
@import '@/assets/css/main.css';
@import '@/assets/css/media.css';
@import '@/assets/css/normalise.css';
</style>
