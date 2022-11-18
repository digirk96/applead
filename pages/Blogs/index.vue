<template>
    <div>
    <Breadcrum  image="./img/about-bg.jpg" />

   <section class="blog">
    <div class="blog-wrapper container">
        <h3>Latest Blogs</h3>

        <div class="card-wrapper">



            <div class="card" v-for="item in blogs" :key="item.id">
                <div class="img-wrapper">
                    <img :src='item.image' :alt="item.image_alt" srcset="">
                </div>
                <div class="card-content">
                    <h4>
                       {{item.title}}
                    </h4>
                    <div class="para" v-html="item.description">
                       
                    </div>

                    <div class="date">

                        <div> <i class="fa-solid fa-calendar"></i><span> 13 May 2022</span></div> <NuxtLink :to="`blogs/${item.slug}`" class="btn"> Read More</NuxtLink>
                    </div>

                </div>

            </div>
           
           
        </div>
    </div>
</section>

    </div>

</template>
<script setup>


const blogs = await fetch(
    'http://127.0.0.1:8000/api/blogs'
).then((res) => res.json()).then(data => data.data)

useHead({
  title: 'My about',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],


})
</script>




<style scoped>
.blog{
    padding: 6rem 0;
        background-color: #fff;
   
}

.blog-wrapper{
    display: flex;
    align-items: center;
    flex-direction: column;
}

.blog-wrapper h3{
        text-align: center;
    margin-bottom: 2rem;
    font-size: 4rem;
    font-weight: 600;
    color: var(--bs-black);
}

.card-wrapper{
    width: 100%;

    display: grid;
    grid-gap: 3rem;
    grid-template-columns: repeat(auto-fill, minmax(32rem, 1fr));
}

.card-wrapper .card{
    padding: 0.8rem;
    background-color: #fff;
    border-radius: 1rem;
    box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}

.card-wrapper .card .img-wrapper{
   height:25rem ;
    border-radius: 1rem;
   


}

.card-wrapper .card .card-content{
 display: flex;
 flex-direction: column;
 gap:1rem;
 padding: 1rem 1rem 0rem 1rem;
   


}

.card-wrapper .card .card-content h4{
           text-align: center;
   
    font-size: 2.2rem;
    font-weight: 600;
    color: var(--bs-black);
}
.card-wrapper .card .card-content .para{
        color: #748494;
    font-size: 1.6rem;
    line-height: 2.5rem;
    text-align: center;
    word-spacing: 2px;
    font-weight: 500;

     overflow: hidden;
  display: -webkit-box;

   text-overflow: ellipsis;
   display: -webkit-box;
   -webkit-line-clamp: 3; /* number of lines to show */
           line-clamp: 3; 
   -webkit-box-orient: vertical;
}

.card-wrapper .card .card-content .date{
    display: flex;
    padding: 1rem ;
  
    justify-content: space-between;
}

.card-wrapper .card .img-wrapper img{
    height: 100%;
    width: 100%;
    object-fit: cover;
        border-radius: 1rem;
}

.btn{
    
    background-color: var(--bs-cyan);
    color: var(--bs-white);
    border: none;
    padding: 0.8rem 2rem;
    width: -moz-fit-content;
    width: fit-content;
    font-size: 1.2rem;
    font-weight: 600;
    border-radius: 0.5rem;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
}


</style>

