<template>
<div>

    <Breadcrum :image="blog.image"/>

    <section class="servicepage">
        <div class="servicepage-wrapper container">
            <div class="left">
                <ServiceContent :title="blog.title" :description="blog.description"></ServiceContent>
                <div class="card-wrapper">
                    <!-- <ServiceCard  v-for="item in service.subservices" :key="item.id" :title="item.title" :icon="item.icon" :path="`${name}/${item.slug}`">

                    </ServiceCard> -->

                </div>
            </div>
            <div class="right">
                <div class="right-top">
                    <h2>Latest Blogs</h2>
                    <ul class="service-list">
                        <ServiceList v-for="item in latestblogs" :key="item.id" :title="item.title" :path="`${item.slug}`"></ServiceList>
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

const latestblogs = await fetch(
    'https://appleadtechnologies.com/applead/api/latestblogs'
).then((res) => res.json()).then(data => data.data)
const blogs = await fetch(
    'https://appleadtechnologies.com/applead/api/blogs'
).then((res) => res.json()).then(data => data.data)


const blog = blogs.find(
    (item) => item.slug === route.params.blog
)

useHead({
  title:blog.pageTitle,
  meta: [
      { name: 'description', content: blog.pageMetaDescription },
        { name: 'title', content: blog.pageMetaTitle }
  ],

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

@media (max-width: 968px){
.servicepage-wrapper {
    flex-direction: column;
}

.left{
    width: 100%;
}
.right{
    align-items: center;
    justify-content: center; width: 100%;
}


}
</style>
