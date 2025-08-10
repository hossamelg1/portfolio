<template>
  <div class="portfolio">
    <div class="container">
      <h1>My Projects</h1>
      <div class="projects-grid">
        <ProjectCard 
          v-for="project in projects" 
          :key="project.id"
          :project="project"
        />
      </div>
    </div>
  </div>
</template>

<script>
import ProjectCard from '../components/ProjectCard.vue'

export default {
  name: 'PortfolioView',
  components: {
    ProjectCard
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Customer Segmentation Analysis',
          description: 'Used K-means clustering to segment customers based on purchasing behavior.',
          technologies: ['Python', 'Scikit-learn', 'Pandas'],
          image: 'https://via.placeholder.com/300x200?text=Customer+Segmentation'
        },
        {
          id: 2,
          title: 'Predictive Maintenance Model',
          description: 'Developed machine learning model to predict equipment failures before they occur.',
          technologies: ['Python', 'TensorFlow', 'Pandas'],
          image: 'https://via.placeholder.com/300x200?text=Predictive+Maintenance'
        },
        {
          id: 3,
          title: 'Sales Forecasting Dashboard',
          description: 'Created interactive dashboard to forecast sales using time series analysis.',
          technologies: ['R', 'Shiny', 'ggplot2'],
          image: 'https://via.placeholder.com/300x200?text=Sales+Forecasting'
        },
        {
          id: 4,
          title: 'Sentiment Analysis of Social Media',
          description: 'Analyzed public sentiment about brands using NLP techniques.',
          technologies: ['Python', 'NLTK', 'Matplotlib'],
          image: 'https://via.placeholder.com/300x200?text=Sentiment+Analysis'
        }
      ]
    }
  }
}
</script>

<style scoped>
.portfolio {
  padding: 40px 0;
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 30px;
  margin-top: 30px;
}
</style>