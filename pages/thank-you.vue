<template>
    <div>
    <Breadcrum  image="./img/about-bg.jpg" />

<h2>Thank You for Reaching Us.<br>We will get back to you soon.</h2>

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
<style scoped>
h2{
    text-align: center;
    display: flex;
    height: 30rem;
    font-size: 3rem;
     line-height: 5rem;
    font-weight: 600;
    color:var(--bs-cyan);
    align-items: center;
    justify-content: center;


}
</style>
