<template>
 <!-- <nav>
 <h2> Balvencia - Onlineshop</h2>
 <RouterLink to="/">Landing</RouterLink> |
 <RouterLink to="/product">Product</RouterLink> |
 <RouterLink to="/about">About</RouterLink> |
 <router-link to="/contact">Contact</router-link>
 </nav>
 <hr /> -->
  <div class="landing-wrapper">
     <!-- Navigation Bar  -->
<header class="navbar">
      <div class="brand-logo">Balvencia — Onlineshop</div>
      <nav class="nav-links">
        <RouterLink to="/" class="nav-item">Landing</RouterLink>
        <RouterLink to="/product" class="nav-item">Product</RouterLink>
        <RouterLink to="/about" class="nav-item">About</RouterLink>
        <RouterLink to="/contact" class="nav-item">Contact</RouterLink>
      </nav>
    </header> 
  </div>
</template>
<script setup>

</script>
<style scoped>
nav {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: nowrap;
    padding: 10px 20px;
}
.landing-wrapper {
  font-family: 'Inter', system-ui, -apple-system, sans-serif;
  max-width: 1100px;
  margin: 0 auto;
  
  color: pink;
}

/* Header & Navbar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 0;
  margin-bottom: 20px;
}
.brand-logo {
  font-weight: 700;
  font-size: 0.95rem;
  color: white;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.nav-item {
  text-decoration: none;
  color: white;
  font-weight: 500;
  font-size: 0.9rem;
  transition: color 0.2s ease;
}

.nav-item:hover {
  color: palevioletred;
}
</style>