<template>
  <header class="header">
    <div class="container">
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/portfolio">Portfolio</router-link>
        <router-link to="/contact">Contact</router-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderView'
}
</script>

<style scoped>
.header {
  background-color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}
nav {
  display: flex;
  justify-content: center;
  gap: 30px;
  padding: 20px 0;
}
a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: color 0.3s;
}
a.router-link-exact-active,
a:hover {
  color: #42b883;
}
</style>