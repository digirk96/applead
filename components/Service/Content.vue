<template>
<div class="content">
    <h2>{{title}}</h2>
    <div class="para" v-html="description">

    </div>
</div>
</template>

<script setup>
const props = defineProps(['description', 'title'])
</script>

<style scoped>
h2 {
    color: var(--bs-black);
    font-weight: 600;
    font-size: 3rem;
}

.para {

    gap: 1rem;
    display: flex;
    flex-direction: column;
    color: #000;
    line-height: 1.6;
}

.para li{
   background-color: #000 !important;
}

.para p {
    color: #748494;
    font-size: 1.6rem;
    line-height: 2.5rem;
    word-spacing: 2px;
    font-weight: 500;
}

.content {
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    flex-direction: column;
    gap: 2rem;
}
</style>
