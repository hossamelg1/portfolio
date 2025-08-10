<template>
  <div class="about">
    <div class="container">
      <h1>About Me</h1>
      <div class="about-content">
        <div class="bio">
          <p>
            I'm a passionate data scientist with expertise in machine learning, 
            statistical analysis, and data visualization. With a background in 
            [your background], I transform complex data into actionable insights.
          </p>
          <p>
            My approach combines technical skills with business acumen to solve 
            real-world problems. I'm constantly learning new technologies and 
            methodologies to stay at the forefront of the data science field.
          </p>
        </div>
        <div class="education">
          <h2>Education</h2>
          <div class="education-item">
            <h3>Degree Name</h3>
            <p>University Name (Year)</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutView'
}
</script>

<style scoped>
.about {
  padding: 40px 0;
}
.about-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 40px;
  margin-top: 30px;
}
.bio p {
  font-size: 1.1rem;
  line-height: 1.6;
  margin-bottom: 20px;
}
.education-item {
  margin-bottom: 20px;
}
.education-item h3 {
  margin-bottom: 5px;
  color: #42b883;
}
@media (max-width: 768px) {
  .about-content {
    grid-template-columns: 1fr;
  }
}
</style>