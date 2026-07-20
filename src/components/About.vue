<template>

<section id="about" class="about">

    <div class="about-content">

<div class="hero-image">
      <img src="../assets/images/d.jpg" alt="Profile Picture" />
    </div>

    <div class="text-content">

        <h2>About Me</h2>

        <p class="intro">
            Hello! I'm Shena Norren, a Bachelor of Science in Information Technology graduate. 
            My journey started with backend development using PHP and MySQL, 
            where I discovered my interest in databases and application logic. 
            Over time, I expanded my skills to frontend development with Vue.js and continue learning 
            by building personal projects like this portfolio. During my college journey, 
            I also gained experience in project documentation and project management. 
            I'm always eager to humbly contribute my skills to meaningful projects while continuing to learn.

        </p>
    </div>
    </div>

        <div class="cards">

            <div class="card">

                <h3>🎓 Education</h3>

                <p>
                    Bachelor of Science in Information Technology
                    <br>
                    <b> Cordova Public College </b>
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

                <h3> What I can do</h3>

                <p class="last-card">
                    Create simple and responsive web interfaces
                    <br>
                    Design relational databases using MySQL
                    <br>
                    Build basic backend logic with PHP
                    <br>
                    Continuously learn and improve my skills
                    <br>
                    Work well with and motivate teammates
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

    color: #CBD5E1;

    line-height:1.8;

    margin-bottom:60px;

    max-width:750px;

    text-align: justify;

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
    color: #CBD5E1;

}
.last-card {
    font-size: 14.5px;
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