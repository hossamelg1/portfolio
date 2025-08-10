<template>
  <div class="home">
    <div class="hero">
      <div class="container">
        <h1>Hi, I'm [Your Name]</h1>
        <p>Data Scientist & Analyst</p>
        <router-link to="/portfolio" class="btn">View My Work</router-link>
      </div>
    </div>
    <div class="container">
      <section class="skills">
        <h2>Skills</h2>
        <div class="skills-grid">
          <div class="skill">Python</div>
          <div class="skill">Machine Learning</div>
          <div class="skill">Data Visualization</div>
          <div class="skill">SQL</div>
          <div class="skill">R</div>
          <div class="skill">Statistics</div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 80px 0;
  text-align: center;
}
.hero h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}
.hero p {
  font-size: 1.5rem;
  margin-bottom: 30px;
}
.skills {
  margin-top: 50px;
}
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.skill {
  background: white;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  text-align: center;
  font-weight: 500;
}
</style>