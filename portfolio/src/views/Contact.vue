<template>
  <div class="contact">
    <div class="container">
      <h1>Contact Me</h1>
      <div class="contact-content">
        <div class="contact-form">
          <form @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">Name</label>
              <input type="text" id="name" v-model="form.name" required>
            </div>
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" id="email" v-model="form.email" required>
            </div>
            <div class="form-group">
              <label for="message">Message</label>
              <textarea id="message" v-model="form.message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn">Send Message</button>
          </form>
        </div>
        <div class="contact-info">
          <h2>Get In Touch</h2>
          <p>Feel free to reach out if you're looking for a data scientist, have a question, or just want to connect.</p>
          <div class="contact-methods">
            <div class="method">
              <strong>Email:</strong> youremail@example.com
            </div>
            <div class="method">
              <strong>LinkedIn:</strong> linkedin.com/in/yourprofile
            </div>
            <div class="method">
              <strong>GitHub:</strong> github.com/yourusername
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactView',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      alert('Form submitted! (This is a demo - in a real app, you would send this to a server)');
      this.form = { name: '', email: '', message: '' };
    }
  }
}
</script>

<style scoped>
.contact {
  padding: 40px 0;
}
.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px;
  margin-top: 30px;
}
.form-group {
  margin-bottom: 20px;
}
.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: 500;
}
.form-group input,
.form-group textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-family: inherit;
}
.contact-info h2 {
  color: #333;
}
.contact-info p {
  line-height: 1.6;
  margin-bottom: 20px;
}
.method {
  margin-bottom: 15px;
  padding: 10px;
  background: white;
  border-radius: 4px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
@media (max-width: 768px) {
  .contact-content {
    grid-template-columns: 1fr;
  }
}
</style>