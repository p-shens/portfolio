<!-- <template>
  <nav class="navbar">
    <div class="logo">
      <h2>Portfolio</h2>
    </div>

    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script setup>
// Nothing here yet
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 20px 80px;

  background: #111827;

  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
}

.logo h2 {
  color: white;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 35px;
}

.nav-links a {
  text-decoration: none;
  color: white;
  transition: 0.3s;
}

.nav-links a:hover {
  color: #3b82f6;
}
</style> -->
<template>
  <nav class="navbar">
    <h2 class="logo">PShens.</h2>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>

.navbar{

display:flex;

justify-content:space-between;

align-items:center;

padding:20px 10%;

background:white;

position:sticky;

top:0;

z-index:1000;

box-shadow:0 2px 10px rgba(0,0,0,.08);

}

.logo{

color:#2563eb;

}

ul{

display:flex;

gap:30px;

list-style:none;

}

a{

text-decoration:none;

color:#333;

font-weight:600;

transition:.3s;

}

a:hover{

color:#2563eb;

}

</style>