<template>
  <div>
   <TheBanner/>
   <About/>
   <Brand/>
   <Portfolio/>
   <Cards />
   <Test/>
   <contact/>
  </div>
</template>
<script setup>


useHead({
  title: 'My Home',
  meta: [
      { name: 'description', content: 'My amazing site.' },
     { name: 'title', content: 'Meta title.' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [ { children: 'console.log(\'Hello world\')' } ]
})
</script>
<style scoped>
.contact {
  padding: 6rem 0;
  background-color: #f8faff;
}

.contact-head {
  text-align: center;
  margin-bottom: 1.8rem;
  font-size: 4rem;
  font-weight: 600;
  color: var(--bs-black);
}

.contact-text {
  text-align: center;
  font-size: 2rem;
  color: #748494;
}

.contact-wrapper {
  margin: 3rem 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
  grid-gap: 2rem;
}

.contact-card {
  flex: 1;
  background-color: var(--bs-white);
  padding: 3rem;
  border-radius: 1rem;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;

  gap: 1.5rem;
}

.contact-card h4 {
  font-size: 1.8rem;
  font-weight: 600;
  color: var(--bs-black);
  margin-bottom: 1rem;
}

.contact-card p {
  font-size: 1.6rem;
  color: #748494;
  line-height: 1.6;
}

.icon {
  font-size: 3.5rem;
}

@media (max-width: 768px) {
  .contact {
    padding: 3rem 0 3rem;
  }

  .contact-head {
    font-size: 3rem;
  }

  .contact-text {
    font-size: 1.6rem;
  }

  .contact-card {
    padding: 1.5rem;
  }

  .contact-card h4 {
    font-size: 1.6rem;
  }

  .contact-card p {
    font-size: 1.4rem;
  }

  .icon {
    font-size: 2.5rem;
  }
}</style>
