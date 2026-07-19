<template>
  <section class="hero">
    <div class="hero-text">
      <p class="greeting">👋 Hello, I'm</p>

      <h1>
        Shena Norren
        <span>Pahugot</span>
      </h1>

      <h2>{{ titles[currentIndex] }}</h2>

      <p class="description">
        Passionate about creating responsive and modern web applications using Vue.js, PHP, MySQL,
        HTML, CSS, and JavaScript.
      </p>

      <div class="buttons">
        
        <a
    href="/resume.pdf"
    download
    class="primary"
>
    Download Resume
</a>

       <a
    href="#projects"
    class="secondary"
>
    View Projects
</a>
      </div>
    </div>

    <div class="hero-image">
      <img src="../assets/images/profile.png" alt="Profile Picture" />
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const titles = [
  "Entry-Level Web Developer",
  "Vue.js Developer",
  "Frontend Developer",
  "IT Graduate"
]

const currentIndex = ref(0)

let intervalId

onMounted(() => {
  intervalId = setInterval(() => {
    if (currentIndex.value === titles.length - 1) {
      currentIndex.value = 0
    } else {
      currentIndex.value++
    }
  }, 3000)
})

onUnmounted(() => {
  clearInterval(intervalId)
})
</script>

<style scoped>

.hero{
    min-height:100vh;

    display:grid;
/* creates two equal columns. */
    grid-template-columns:1fr 1fr;

    align-items:center;

    gap:60px;

    padding:120px 8% 60px;
}

.hero-text{
    animation:fadeLeft .8s ease;
}

.hero-image{
    display:flex;
    justify-content:center;

    animation:fadeRight .8s ease;
}

.hero-image img{

    width:350px;

    height:350px;

    object-fit:cover;

    border-radius:50%;

    border:5px solid var(--primary);

    box-shadow:0 0 30px rgba(59,130,246,.3);

}

.greeting{

    color:var(--primary);

    font-size:22px;

    margin-bottom:15px;

}

h1{

    font-size:64px;

    line-height:1.1;

    margin-bottom:15px;

}

h1 span{

    color:var(--primary);

}

h2{

    color:var(--secondary);

    margin-bottom:25px;

    font-weight:500;

}

.description{

    color:#CBD5E1;

    line-height:1.8;

    max-width:550px;

    margin-bottom:35px;

}

.buttons{

    display:flex;

    gap:20px;

}

a{

    padding:15px 32px;

    border-radius:8px;

    font-size:16px;

    transition:.3s;

}

.primary{

    background:var(--primary);

    border:none;

    color:white;

}

.primary:hover{

    transform:translateY(-5px);

}

.secondary{

    background:transparent;

    color:white;

    border:2px solid var(--primary);

}

.secondary:hover{

    background:var(--primary);

}

@keyframes fadeLeft{

from{

opacity:0;

transform:translateX(-50px);

}

to{

opacity:1;

transform:translateX(0);

}

}

@keyframes fadeRight{

from{

opacity:0;

transform:translateX(50px);

}

to{

opacity:1;

transform:translateX(0);

}

}

@media(max-width:900px){

.hero{

grid-template-columns:1fr;

text-align:center;

}

.hero-image{

order:-1;

}

.buttons{

justify-content:center;

}

}

</style>
