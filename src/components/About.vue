<template>

<section id="about" class="about">

    <div class="about-content">

<div class="hero-image">
      <img src="" alt="Profile Picture" />
    </div>

    <div class="text-content">

        <h2>About Me</h2>

        <p class="intro">
            I am a Bachelor of Science in Information Technology graduate who
            enjoys building responsive and user-friendly web applications.
            I am continuously improving my skills in Vue.js, JavaScript,
            PHP, and modern web development.
        </p>
    </div>
    </div>

        <div class="cards">

            <div class="card">

                <h3>🎓 Education</h3>

                <p>
                    Bachelor of Science in Information Technology
                </p>

            </div>

            <div class="card">

                <h3>💼 Experience</h3>

                <p>
                    Import & Export Declarant
                    <br>
                    Billing In-Charge
                </p>

            </div>

            <div class="card">

                <h3>❤️ Passion</h3>

                <p>
                    Web Development
                    <br>
                    Learning New Technologies
                    <br>
                    Problem Solving
                </p>

            </div>

        </div>

    

</section>

</template>

<script setup>

</script>

<style scoped>

.about{
    padding:120px 8%;

    display:flex;

    flex-direction:column;

    gap:60px;
}

.about-content{
    display:flex;

    align-items:center;

    gap:80px;
}

h2{

    font-size:42px;

    margin-bottom:20px;

    color:var(--primary);

}

.intro{

    color:#CBD5E1;

    line-height:1.8;

    margin-bottom:60px;

    max-width:750px;

}

.cards{

    display:grid;

    grid-template-columns:repeat(3,1fr);

    gap:30px;

}

.card{

    background:var(--card);

    padding:35px;

    border-radius:15px;

    transition:.3s;

}

.card:hover{

    transform:translateY(-10px);

}

.card h3{

    margin-bottom:20px;

}

.card p{

    line-height:1.8;

}

@media (max-width:900px){

.about-content{

    flex-direction:column;

    text-align:center;

}

.cards{

    grid-template-columns:1fr;

}

}
.hero-image{
    display:flex;
    justify-content:center;

    animation:fadeRight .8s ease;
}

.hero-image img{

    width:250px;

    height:250px;

    object-fit:cover;

    border-radius:50%;

    border:5px solid var(--primary);

    box-shadow:0 0 30px rgba(59,130,246,.3);

}



</style>