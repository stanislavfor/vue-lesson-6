<template>
  <div class="wrapper">
    <Header :navLinks="navLinks" />
    <main class="main">
      <section class="main-blog-details-section"></section>
      <section class="main-blog-details">
        <div class="blog-details">
          <blog-posts :posts="filteredPosts"></blog-posts>
        </div>
        <div class="sidebar">
          <h2>Тэги</h2>
          <button class="smooth-button" v-for="tag in tags" :key="tag" @click="filterPosts(tag)">{{ tag }}</button>
          <button class="smooth-button" @click="filterPosts('')">Все Тэги</button>
        </div>
      </section>
    </main>
    <Footer :footerLinks="footerLinks" />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'BlogDetailsComponent',
  components: {
    Header,
    Footer,
    'blog-posts': {
      props: ['posts'],
      template: `
        <div>
          <div v-for="post in posts" :key="post.title">
            <h2>{{ post.title }}</h2>
            <p class="blog-details__article-date">{{ post.date }}</p>
            <p class="blog-details__article-tags">{{ post.tag }}</p>
            <div v-for="(content, index) in post.content" :key="index">
              <picture v-if="content.type === 'img'">
                <img class="blog-details__article-img" :src="content.src" alt="">
              </picture>
              <p v-if="content.type === 'text'" class="blog-details__article-text">{{ content.text }}</p>
            </div>
          </div>
        </div>
      `
    }
  },
  data() {
    return {
      selectedTag: '',
      navLinks: [
        { text: 'Проекты', href: 'projects.html' },
        { text: 'Блог', href: 'blog.html' },
        { text: 'Домой', href: 'index.html#main-section' },
        { text: 'Контакты', href: '#contact-section' }
      ],
      footerLinks: [
        { text: 'Домой', href: 'index.html#main-section' },
        { text: 'Проекты', href: 'projects.html' },
        { text: 'Блог', href: 'blog.html' },
        { text: 'Наши успехи', href: 'index.html#achievements' }
      ],
      posts: [
        {
          title: 'Создадим лучший макет перепланировки',
          date: '26 Декабря, 2024',
          tag: 'Кухня',
          content: [
            { type: 'img', src: require('@/assets/images/details-1.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium orci vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Fusce vel interdum elit, at congue lorem. Vestibulum pellentesque, orci in gravida fermentum, purus libero varius urna, ut vehicula velit nulla a nisl. Sed aliquet, nisi eget sagittis tincidunt, nisi elit consectetur nunc, ut congue nisl nisi vitae nunc. Proin consectetur, nisi id ullamcorper varius, nisi nisi aliquam nisi, eget aliquam nisi nisi eget nisi.' },
            { type: 'img', src: require('@/assets/images/details-2.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium orci vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Fusce vel interdum elit, at congue lorem. Vestibulum pellentesque, orci in gravida fermentum, purus libero varius urna, ut vehicula velit nulla a nisl. Sed aliquet, nisi eget sagittis tincidunt, nisi elit consectetur nunc, ut congue nisl nisi vitae nunc. Proin consectetur, nisi id ullamcorper varius, nisi nisi aliquam nisi, eget aliquam nisi nisi eget nisi.' }
          ]
        },
        {
          title: 'Design sprints are great',
          date: '22 Декабря, 2024',
          tag: 'Дизайн',
          content: [
            { type: 'img', src: require('@/assets/images/details-3.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium orci vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Fusce vel interdum elit, at congue lorem. Vestibulum pellentesque, orci in gravida fermentum, purus libero varius urna, ut vehicula velit nulla a nisl. Sed aliquet, nisi eget sagittis tincidunt, nisi elit consectetur nunc, ut congue nisl nisi vitae nunc. Proin consectetur, nisi id ullamcorper varius, nisi nisi aliquam nisi, eget aliquam nisi nisi eget nisi.' },
            { type: 'img', src: require('@/assets/images/details-4.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' }
          ]
        },
        {
          title: 'Лучшие интерьерные идеи по низкой цене',
          date: '22 Декабря, 2024',
          tag: 'Здания',
          content: [
            { type: 'img', src: require('@/assets/images/details-5.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' },
            { type: 'img', src: require('@/assets/images/details-6.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' }
          ]
        },
        {
          title: 'Спальные интерьеры и возможности дизайнеров',
          date: '9 Декабря, 2024',
          tag: 'Спальня',
          content: [
            { type: 'img', src: require('@/assets/images/details-7.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' }
          ]
        },
        {
          title: 'Лучшие интерьерные решения для офисов',
          date: '25 Декабря, 2024',
          tag: 'Архитектура',
          content: [
            { type: 'img', src: require('@/assets/images/details-8.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' }
          ]
        },
        {
          title: 'Жизнь без дизайнерских решений',
          date: '10 Декабря, 2024',
          tag: 'Архитектура',
          content: [
            { type: 'img', src: require('@/assets/images/details-9.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.' }
          ]
        },
        {
          title: 'Квартиры и офисы - делаем лучше',
          date: '05 Декабря, 2024',
          tag: 'Планировка',
          content: [
            { type: 'img', src: require('@/assets/images/details-10.png') },
            { type: 'text', text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nisl eros, pulvinar facilisis justo mollis, auctor consequat urna. Morbi a bibendum metus. Donec scelerisque sollicitudin enim eu venenatis. Duis tincidunt laoreet ex, in pretium vestibulum eget. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Aliquam volutpat aliquam luctus. Pellentesque vitae aliquam nunc. Sed laoreet metus nec purus luctus, quis luctus lorem consequat. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Fusce vel interdum elit, at congue lorem. Vestibulum pellentesque, orci in gravida fermentum, purus libero varius urna, ut vehicula velit nulla a nisl. Sed aliquet, nisi eget sagittis tincidunt, nisi elit consectetur nunc, ut congue nisl nisi vitae nunc. Proin consectetur, nisi id ullamcorper varius, nisi nisi aliquam nisi, eget aliquam nisi nisi eget nisi.' },
            { type: 'img', src: require('@/assets/images/details-11.png') }
          ]
        }
      ],
      tags: ['Кухня', 'Спальня', 'Здания', 'Архитектура', 'Планировка', 'Дизайн']
    };
  },
  computed: {
    filteredPosts() {
      if (this.selectedTag) {
        return this.posts.filter(post => post.tag === this.selectedTag);
      }
      return this.posts;
    }
  },
  methods: {
    filterPosts(tag) {
      this.selectedTag = tag;
    }
  }
};
</script>

<style scoped>
/* Add "scoped" attribute to limit CSS to this component only */
@import '@/assets/css/main.css';
@import '@/assets/css/media.css';
@import '@/assets/css/normalise.css';
</style>
