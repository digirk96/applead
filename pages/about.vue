<template>
    <div>
    <Breadcrum  image="./img/about-bg.jpg" title="About Us"/>

   <About/>

    </div>

</template>
<script setup>


useHead({
  title: 'My about',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],


})
</script>
