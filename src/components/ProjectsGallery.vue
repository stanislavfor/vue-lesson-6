<template>
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
</template>

<script>
export default {
  name: 'ProjectsGallery',
  props: {
    projects: {
      type: Array,
      required: true
    },
    selectedTag: {
      type: String,
      required: true
    }
  },
  computed: {
    filteredProjects() {
      if (this.selectedTag) {
        return this.projects.filter(project => project.tag === this.selectedTag);
      }
      return this.projects;
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
