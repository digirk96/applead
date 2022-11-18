<template>
<nuxt-link :to="path" class="card">
   <div class="icon" v-html="icon">

    </div>
    <h3>
        {{title}}
    </h3>

</nuxt-link>

</template>

<script setup>

const props = defineProps(['icon', 'title', 'path'])
</script>

<style scoped>
.card {
    border: 1px solid #e7e7e7;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    background-color: #fcfcfc;
    padding: 1rem 1.5rem;

}

.icon {
    color: #5fe9f2;
    font-size: 1.8rem;
}

h3 {
    font-size: 1.6rem;
    font-weight: 400;
    text-transform: capitalize;
}
</style>
