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
            :demoUrl="project.demoUrl"
            :githubUrl="project.githubUrl"
        />

    </div>

</section>

</template>

<script setup>

import ProjectCard from "./ProjectCard.vue"
import lostFound from '../assets/projects/lf.png'

const projects = [

{
    id:1,

    image: lostFound,

    title:"Lost & Found Management System",

    status: "Completed",

    description:"A responsive web application that allows students and staff to report, search, and track lost and found items.",

    tech: [
  "Vue.js",
  "PHP",
  "MySQL"
],
demoUrl:"#",

    githubUrl:"https://github.com/yourusername/lost-found"
},

{
    id:2,

    image:"https://picsum.photos/600/400?2",

    title:"Personal Portfolio",

    status: "In Progress",

    description:"A responsive portfolio website showcasing my projects and skills.",

    tech: [
  "Vue.js",
  "PHP",
  "MySQL"
],
demoUrl:"#",

    githubUrl:"https://github.com/yourusername/lost-found"
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

}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(350px,1fr));
gap:35px;
margin-top:50px;
}

</style>