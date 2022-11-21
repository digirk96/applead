<template>
 <footer class="footer">
      <div class="container">
        <div class="footer-cols">
          <div class="link-foot">
               <h3>About Applead</h3>
            <p>
               AppLead Technologies is a fast growing mobile app development company at the helm of latest technology breakthroughs and led by a competent technical team.
            </p>
            <ul class="social">
              <li><a href=""><i class="fa-brands fa-facebook"></i></a></li>
              <li><a href=""><i class="fa-brands fa-linkedin"></i></a></li>
              <li><a href=""><i class="fa-brands fa-instagram"></i></a></li>
              <li><a href=""><i class="fa-brands fa-twitter"></i></a></li>
            </ul>
          </div>
          <ul class="link-foot">
              <h3>Quick Links</h3>
              <li class="link">
                 <NuxtLink to="/">Home</NuxtLink>
              </li>
              <li class="link">
                 <NuxtLink to="/about">About</NuxtLink>
              </li>
               <li class="link">
                 <NuxtLink to="/services">Services</NuxtLink>
              </li>
               <li class="link">
                 <NuxtLink to="/blogs">Blogs</NuxtLink>
              </li>
               <li class="link">
                 <NuxtLink to="/contact">Contact</NuxtLink>
              </li>
          </ul>
          <ul class="link-foot">
          <h3>Latest Services</h3>
           <li class="link" v-for="item of services" :key="item.id">
                 <NuxtLink :to="`/services/${item.slug}`"> {{item.title}}</NuxtLink>
              </li>
            
          </ul>
          <ul class="link-foot">
          <h3>Latest Blogs</h3>

           <li class="link" v-for="item of blogs" :key="item.id">
                 <NuxtLink :to="`/blogs/${item.slug}`">{{item.title}}</NuxtLink>
              </li>
              
          </ul>
        </div>

        <p class="footer-content">
          &copy; <span>2022 by </span>
          <span class="highlight">AppLead</span>
        </p>
      </div>
    </footer>
</template>
<script setup>

const blogs = await fetch(
    'https://appleadtechnologies.com/applead/api/blogs'
).then((res) => res.json()).then(data => data.data)

const services = await fetch(
    'https://appleadtechnologies.com/applead/api/service'
).then((res) => res.json()).then(data => data.data)
useHead({
 
link: [
      {
        rel:"stylesheet", href:"https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.0/css/all.min.css", integrity:"sha512-xh6O/CkQoPOWDdYTDqeRdPCVd1SpvCA9XXcUnZS2FmJNp1coAFzvtCN9BmamE+4aHK8yyUHUSCcJHgXloTyT2A==", crossorigin:"anonymous", referrerpolicy:"no-referrer"
      }
    ]
})
</script>

<style scoped>
.footer {
  background-color: var(--bs-secondary);
  padding: 3rem 0;
}

.footer-cols{
  display: grid;
     grid-template-columns: repeat(auto-fill, minmax(26rem, 1fr));
     color: rgba(255, 255, 255, 0.704);
     margin-bottom: 2rem;
     grid-gap: 3rem;
 
}

.footer-cols .link-foot{
  display: flex;
  flex-direction: column;
  gap:1.5rem;
  font-size: 1.4rem;
}

.footer-cols .link-foot h3{
  font-size: 2rem;
  color: white;
}


.footer-cols .link-foot p{
  text-align: justify;
}

.social{
  display: flex;
  gap:3rem;
  font-size: 2.5rem;
  color: rgba(255, 255, 255, 0.862);
}

.footer-cols .link-foot .link{
  list-style: disc;
  margin-left: 2rem;
}





.footer-content {
     border-top:  1px solid rgba(255, 255, 255, 0.301);
  text-align: center;
  color: var(--bs-white);
  font-size: 2rem;
  padding-top: 2rem;
}

.footer-content span {
  font-size: 1.5rem;

  margin-top: 0.5px;
}

.highlight {
  color: var(--bs-primary);
}</style>

