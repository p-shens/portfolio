<template>
  <section id="contact" class="contact">

    <h1>Contact Information</h1>


    <div class="contact-list">

      <a
        v-for="contact in contacts"
        :key="contact.label"
        :href="contact.url"
        target="_blank"
        class="contact-card"
      >
        <span class="icon">{{ contact.icon }}</span>

        <div>
          <h3>{{ contact.label }}</h3>
        </div>

      </a>

    </div>

  </section>
</template>

<script setup>

const contacts = [

  {
    icon: "📧",
    label: "Email",
    url: "mailto:pahugotshena31@gmail.com"

  },
  {
    icon: "📞",
    label: "Phone Number",
    url: "63+ 9329123656"
  },
  {
    icon: "🌐",
    label: "Facebook",
    url: "https://www.facebook.com/p.shens29"
  }

]

</script>

<style scoped>

.contact{
    padding:80px 10%;
    text-align:center;
}
.contact h1{
    color:var(--primary);
    margin-bottom:40px;
}    

.contact-list{

    display:grid;

    grid-template-columns:repeat(auto-fit,minmax(260px,1fr));

    gap:25px;

}

.contact-card{

    display:flex;

    align-items:center;

    gap:20px;

    text-decoration:none;

    color:#333;

    background:white;

    padding:20px;

    border-radius:15px;

    box-shadow:0 5px 15px rgba(0,0,0,.08);

    transition:.3s;

}

.contact-card:hover{

    transform:translateY(-5px);

}

.icon{

    font-size:2rem;

}

.contact-card h3{

    margin:0;

}

.contact-card p{

    margin-top:5px;

    color:#666;

}


</style>