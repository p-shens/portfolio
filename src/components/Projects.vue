<template>

<section id="projects" class="projects">

    <h1>My Projects</h1>

    <div class="grid">

        <ProjectCard
            v-for="project in projects"
            :key="project.id"
            :image="project.image"
            :title="project.title"
            :status="project.status"
            :description="project.description"
            :tech="project.tech"
            :githubUrl="project.githubUrl"
        />

    </div>

</section>

</template>

<script setup>

import ProjectCard from "./ProjectCard.vue"
import lostFound from '../assets/projects/lf.png'
import portfolio from '../assets/projects/portfolio.png'
import crud from '../assets/projects/PHP.png'

const projects = [

{
    id:1,

    image:portfolio,

    title:"Personal Portfolio (2026)",

    status: "In Progress",

    description:"This portfolio was built using Vue.js to showcase my projects, skills, and learning journey as a web developer. It also helped me strengthen my frontend development skills by building a responsive and modern website from scratch.",

    tech: [ "Vue.js" ],

    demoUrl:"#",

    githubUrl:"https://github.com/p-shens/portfolio"
},

{
    id:2,

    image: lostFound,

    title:"Lost & Found Management System | Capstone Project (2024)",

    status: "Completed",

    description:"This was our capstone project in 2024, created to help students and staff easily report, search for, and track lost and found items on campus. I focused mainly on the backend development, database design, and application logic, while also helping connect the backend to the frontend.",

    tech: [
        "Vue.js",
        "CSS",
        "Quasar",
        "PHP",
        "MySQL"
    ],

    githubUrl:"https://github.com/p-shens/lost-and-found-system-backend"
},

{
    id: 3,

    image: crud,

    title:"CRUD Project (2024)",

    status: "Archived",

    description:"This is a CRUD web application built with native PHP using the MVC pattern. It includes user authentication, password encryption, and database backup functionality.",
    tech: [ "HTML", "CSS", "PHP" ],

    demoUrl:"#",

    githubUrl:"https://github.com/yourusername/"
}

]

</script>

<style scoped>

.projects{

padding:60px 10%;

}

.projects h1{

text-align:center;

margin-bottom:40px;

color:var(--primary);

}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(350px,1fr));
gap:35px;
margin-top:50px;
}

</style>