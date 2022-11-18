<template>
 <section className="breadcrum">
      <img :src=image alt="about" />
    </section>
</template>

<script setup>
const props = defineProps([
    'image'
])

</script>

<style  scoped>
.breadcrum {
  margin-top: 10rem;
  height: 45rem;
  width: 100%;
  position: relative;
}

.breadcrum::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  background-color: var(--bs-overlay-black);
  opacity: 0.5;
}



.breadcrum img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

</style>
