<template>
  <footer class="footer">

    <p>
      © {{ currentYear }} PS. All rights reserved.
    </p>

    <a href="#hero" class="back-to-top">
      ↑ Back to Top
    </a>

  </footer>
</template>

<script setup>
const currentYear = new Date().getFullYear()
</script>

<style scoped>

.footer{
    padding:40px 10%;
    text-align:center;
    border-top:1px solid #e5e7eb;
    margin-top:80px;
}

.footer p{
    margin:10px 0;
    color:#64748b;
}

.built-with{
    font-size:14px;
}

.back-to-top{
    display:inline-block;
    margin-top:20px;
    text-decoration:none;
    color:var(--primary);
    font-weight:600;
}

.back-to-top:hover{
    text-decoration:underline;
}

</style>