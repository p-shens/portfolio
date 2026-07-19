<template>

<section id="skills" class="skills">

    <h1>Technical Skills</h1>

    <div class="skills-grid">

        <div
            v-for="category in skillCategories"
            :key="category.title"
            class="skill-card"
        >

            <h2>{{ category.title }}</h2>

            <div class="badges">

                <span
                    v-for="skill in category.skills"
                    :key="skill"
                    class="badge"
                >
                    {{ skill }}
                </span>

            </div>

        </div>

    </div>

</section>

</template>

<script setup>

const skillCategories = [

{
    title:"Frontend",

    skills:[
        "HTML",
        "CSS",
        "JavaScript",
        "Vue.js"
    ]
},

{
    title:"Backend",

    skills:[
        "PHP",
        "MySQL"
    ]
},

{
    title:"Tools",

    skills:[
        "Git",
        "GitHub",
        "VS Code",
        "XAMPP",
        "Microsoft Excel"
    ]
}

]

</script>

<style scoped>

.skills{

padding:80px 10%;

}

.skills h1{

text-align:center;

margin-bottom:50px;

}

.skills-grid{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(300px,1fr));

gap:30px;

}

.skill-card{

background:white;

padding:30px;

border-radius:15px;

box-shadow:0 5px 15px rgba(0,0,0,.08);

}

.badges{

display:flex;

flex-wrap:wrap;

gap:10px;

margin-top:20px;

}

.badge{

background:#2563eb;

color:white;

padding:8px 16px;

border-radius:30px;

font-size:14px;

}

</style>