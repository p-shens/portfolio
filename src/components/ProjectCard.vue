<template>
  <div class="project-card">
    <img
      :src="image"
      :alt="title"
      class="project-image"
    />

    <div class="project-content">
      <h2>{{ title }}</h2>

      <span
    v-if="status === 'Completed'"
    class="status completed"
>
    {{ status }}
</span>

<span
    v-else-if="status === 'In Progress'"
    class="status in-progress"
>
    {{ status }}
</span>

<span
    v-else-if="status === 'Archived'"
    class="status in-archived"
>
    {{ status }}
</span>


      <p>{{ description }}</p>

     <div class="tech-container">
        <span
            v-for="tag in tech"
            :key="tag"
            class="tech"
        >
        {{ tag }}    
             </span>

     </div>

    <div class="buttons">

    <a
        :href="githubUrl"
        target="_blank"
         rel="noopener noreferrer"
        class="btn secondary"
    >
        GitHub
    </a>

</div>
      
    </div>
  </div>
</template>


<script setup>
const {
    image,
    title,
    description,
    tech,
    githubUrl,
    status
} = defineProps({
    image: String,
    title: String,
    description: String,
    tech: Array,
    githubUrl: String,
    status: String
})
</script>

<style scoped>

.project-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  transition: 0.3s;
  box-shadow: 0 8px 20px rgba(0,0,0,.08);
}

.project-card:hover {
  transform: translateY(-8px);
}

.project-image {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.project-content {
  padding: 24px;
}

.project-content h2 { 
  margin-bottom: 12px;
}

.project-content p {
  color: #555;
  line-height: 1.6;
  text-align: justify;
}

.tech {
  background: #2563eb;
  color: white;
  padding: 6px 14px;
  border-radius: 999px;
  font-size: 14px;
  font-weight: 500;
}

.tech-container {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 20px;
}

.buttons{

display:flex;

gap:12px;

margin-top:25px;

}

.btn{

text-decoration:none;

padding:10px 18px;

border-radius:10px;

font-weight:bold;

transition:.3s;

}

.primary{

background:#2563eb;

color:white;

}

.secondary{

background:#e5e7eb;

color:#111827;

}

.btn:hover{

transform:translateY(-3px);

}
.project-content h2 {
  color: #111827;
  margin-bottom: 12px;
}

.status{
    display:inline-block;

    padding:6px 12px;

    border-radius:999px;

    background:#DCFCE7;

    color:#166534;

    font-size:14px;

    font-weight:600;

    margin-bottom:cpx;
}
.status{

    display:inline-block;

    padding:6px 12px;

    border-radius:999px;

    font-size:13px;

    font-weight:600;

    margin-bottom: 16px;

}

.completed{

    background:#DCFCE7;

    color:#166534;

}

.in-progress{

    background:#ebc1c1;

    color:#802d27;

}
.in-archived{

    background:#f3f4f6;

    color:#374151;

}



</style>