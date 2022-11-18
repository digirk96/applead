<template>
    <div>
 <Breadcrum  image="./img/contact-bg.jpg" />
   <Contact/>

    </div>
</template>
<script setup>


useHead({
  title: 'My contact',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [ { children: 'console.log(\'Hello world\')' } ]
})
</script>

<style lang="scss" scoped>

</style>
