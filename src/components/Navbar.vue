<template>
  <nav class="navbar">
    <h2 class="logo">PShens.</h2>

    <ul>
      <li><a href="#hero">Home</a></li>
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

color:var(--primary);

}

ul{

display:flex;

gap:30px;

list-style:none;

}

a{

text-decoration:none;

color:#111827;

font-weight:600;

transition:.3s;

}

a:hover{

color:var(--primary);

}

</style>