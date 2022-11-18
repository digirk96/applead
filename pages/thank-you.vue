<template>
    <div>
    <Breadcrum  image="./img/about-bg.jpg" />

<h2>Thank You </h2>

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
    font-size: 4rem;
    font-weight: 600;
    color:var(--bs-cyan);
    align-items: center;
    justify-content: center;


}
</style>
