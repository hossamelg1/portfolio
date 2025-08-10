<template>
  <div class="project-card">
    <img :src="project.image" :alt="project.title">
    <div class="project-info">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
      <div class="technologies">
        <span 
          v-for="tech in project.technologies" 
          :key="tech"
          class="tech-tag"
        >
          {{ tech }}
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    project: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.project-card {
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s;
}
.project-card:hover {
  transform: translateY(-5px);
}
.project-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.project-info {
  padding: 20px;
}
.project-info h3 {
  margin-top: 0;
  color: #333;
}
.project-info p {
  color: #666;
  line-height: 1.5;
}
.technologies {
  margin-top: 15px;
}
.tech-tag {
  display: inline-block;
  background: #e0f7e9;
  color: #42b883;
  padding: 5px 10px;
  border-radius: 20px;
  font-size: 0.8rem;
  margin-right: 8px;
  margin-bottom: 8px;
}
</style>