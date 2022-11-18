<template>
<div>

    <Breadcrum :image="subservice.image" />

    <section class="servicepage">
        <div class="servicepage-wrapper container">
            <div class="left">
                <ServiceContent :title="subservice.title" :description="subservice.description"></ServiceContent>
                <div class="card-wrapper">
                    <ServiceCard  v-for="item in subservice.subsubservices" :key="item.id" :title="item.title" :icon="item.icon" :path="`${name}/${item.slug}`">

                    </ServiceCard>

                </div>
            </div>
            <div class="right">
                <div class="right-top">
                    <h2>Our Sub Services</h2>
                    <ul class="service-list">
                        <ServiceList v-for="item in service.subservices" :key="item.id" :title="item.title" :path="`${item.slug}`"></ServiceList>
                    </ul>
                </div>
                <ServiceForm></ServiceForm>

            </div>

        </div>
    </section>


</div>


</template>

<script setup>



const route = useRoute()


const name = computed(() => {
    return route.params.slug
})

const services = await fetch(
    'https://appleadtechnologies.com/applead/api/service'
).then((res) => res.json()).then(data => data.data)

const subservices = await fetch(
    'https://appleadtechnologies.com/applead/api/subservice'
).then((res) => res.json()).then(data => data.data)

const subservice = subservices.find(
    (item) => item.slug === route.params.slug
)
const service = services.find(
    (item) => item.slug === subservice.service_slug
)

useHead({
  title:subservice.pageTitle,
  meta: [
      { name: 'description', content: subservice.pageMetaDescription },
        { name: 'title', content: subservice.pageMetaTitle }
  ],
  bodyAttrs: {
    class: 'test'
  },
link: [
      {
        rel:"stylesheet", href:"https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css", integrity:"sha512-xh6O/CkQoPOWDdYTDqeRdPCVd1SpvCA9XXcUnZS2FmJNp1coAFzvtCN9BmamE+4aHK8yyUHUSCcJHgXloTyT2A==", crossorigin:"anonymous", referrerpolicy:"no-referrer"
      }
    ]
})


</script>

<style scoped>
.servicepage {
    width: 100%;
    padding: 6rem 0;
}

.servicepage-wrapper {

    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 4rem;
}

.left {
    width: 78rem;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    flex-direction: column;
    gap: 2rem;
}

.card-wrapper {
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 1.5rem;
    flex-wrap: wrap;
}

.right {
    width: 38rem;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 3rem;
}

.right-top {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
}

h2 {
    color: var(--bs-black);
    font-weight: 600;
    font-size: 3rem;
    margin-bottom: 1.5rem;
}

.service-list {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 1rem;
}
</style>
