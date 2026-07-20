<template>
  <section id="hero" class="hero">

    <!-- Left Side -->
    <div class="hero-text">

      <p class="greeting">
        👋 This is,
      </p>

      <h1>
        Shena Norren
        <span>Pahugot</span>
      </h1>

      <h2 class="title">
        {{ titles[currentIndex] }}
      </h2>

      <div class="buttons">

        <a
          href="/PAHUGOT SHENA NORREN.pdf"
          download
          class="btn primary"
        >
          Download Resume
        </a>

        <a
          href="#projects"
          class="btn secondary"
        >
          View Projects
        </a>

      </div>

    </div>

  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue"

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

  }, 2500)

})

onUnmounted(() => {

  clearInterval(intervalId)

})
</script>

<style scoped>

.hero{

    min-height:100vh;

    display:grid;

    align-items:center;

    gap:80px;

    padding:120px 10% 80px;
    

}

.hero-text{

    animation:fadeLeft .8s ease;

}

.greeting{

    color:var(--primary);

    font-size:22px;

    margin-bottom:15px;

    font-weight:600;

}

h1{

    font-size:64px;

    line-height:1.1;

    margin-bottom:15px;

}

h1 span{

    color:var(--primary);

}

.title{

    color:var(--secondary);

    font-size:30px;

    font-weight:600;

    margin-bottom:25px;

    min-height:40px;

}

.description{

    color:var(--text-muted);

    line-height:1.8;

    max-width:550px;

    margin-bottom:40px;

}

.buttons{

    display:flex;

    gap:20px;

}

.btn{

    display:inline-flex;

    align-items:center;

    justify-content:center;

    padding:15px 30px;

    border-radius:10px;

    text-decoration:none;

    font-weight:600;

    transition:.3s;

}

.primary{

    background:var(--primary);

    color:white;

}

.primary:hover{

    transform:translateY(-5px);

}

.secondary{

    border:2px solid var(--primary);

    color:white;

}

.secondary:hover{

    background:var(--primary);

}

.hero-image{

    display:flex;

    justify-content:center;

    animation:fadeRight .8s ease;

}

.hero-image img{

    width:360px;

    max-width:100%;

    aspect-ratio:1/1;

    object-fit:cover;

    border-radius:50%;

    border:5px solid var(--primary);

    box-shadow:0 0 40px rgba(34,197,94,.25);

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

gap:40px;

}

.hero-image{

order:-1;

}

.buttons{

justify-content:center;

flex-wrap:wrap;

}

h1{

font-size:48px;

}

.title{

font-size:24px;

}

}

</style>