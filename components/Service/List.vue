<template>
<li>
      <nuxt-link :to="path">{{title}}</nuxt-link>
</li>
</template>

<script setup>

const props = defineProps(['path', 'title'])
</script>

<style scoped>
li {
    padding: 1.5rem;

    width: 100%;
    background-color: #527abc;
}

li:first-child {
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
}

li:nth-last-child(1) {
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
}

a {
    width: 100%;
    font-size: 1.4rem;
    color: #fff;
}
</style>
