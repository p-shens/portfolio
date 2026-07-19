<template>
  <section id="skills" class="skills">

    <h1>Technologies I Work With</h1>

    <p class="subtitle">
      These are the technologies I've used throughout my academic projects and personal learning journey.
    </p>

    <div class="skills-grid">

      <div
        v-for="skill in skills"
        :key="skill.name"
        class="skill-card"
      >

        <i :class="skill.icon"></i>

        <h2>{{ skill.name }}</h2>

        <p>{{ skill.description }}</p>

      </div>

    </div>

  </section>
</template>

<script setup>

const skills = [

{
    name: "PHP",
    icon: "devicon-php-plain colored",
    description: "I use PHP to build the backend of my projects. I'm comfortable with native PHP and organizing my code using the MVC pattern, and I'm still learning more as I build new projects."
},

{
    name: "MySQL",
    icon: "devicon-mysql-plain colored",
    description: "I enjoy working with databases and designing tables. Most of my projects use MySQL to store and manage data."
},

{
    name: "Vue.js",
    icon: "devicon-vuejs-plain colored",
    description: "I use Vue.js to build responsive and interactive user interfaces. I'm still learning more about Vue, and building this portfolio has helped me improve a lot."
},

{
    name: "JavaScript",
    icon: "devicon-javascript-plain colored",
    description: "I use JavaScript to make my web applications interactive and connect the frontend with the backend."
},

{
    name: "Express.js",
    icon: "devicon-express-original",
    description: "I have basic knowledge of Express.js from our college projects and I'm excited to learn more."
},

{
    name: "Node.js",
    icon: "devicon-nodejs-plain colored",
    description: "I learned the basics of Node.js and used it together with Express.js in one of our school projects."
}

]

</script>

<style scoped>

.skills{

    padding:100px 10%;

}

.skills h1{

    text-align:center;

    font-size:42px;

    margin-bottom:15px;

    color:var(--primary);

}

.subtitle{

    text-align:center;

    color:#94A3B8;

    max-width:700px;

    margin:0 auto 60px;

    line-height:1.7;

}

.skills-grid{

    display:grid;

    grid-template-columns:repeat(auto-fit,minmax(320px,1fr));

    gap:30px;

}

.skill-card{

    background:var(--card);

    padding:35px;

    border-radius:18px;

    transition:.3s;

    border:1px solid rgba(255,255,255,.08);

}

.skill-card:hover{

    transform:translateY(-8px);

    box-shadow:0 10px 30px rgba(0,0,0,.2);

}

.skill-card i{

    font-size:55px;

    margin-bottom:20px;

    display:block;

}

.skill-card h2{

    margin-bottom:15px;

    color:white;

}

.skill-card p{

    color:#CBD5E1;

    line-height:1.7;

}

@media(max-width:768px){

.skills{

padding:80px 8%;

}

}

</style>