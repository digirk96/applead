<template>
    <section class="hero">


  <swiper
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: true,
    }"
    :navigation="false"
    :modules="modules"
    class="mySwiper"
  >
           <SwiperSlide
          class="banner"
         style="background-image:url('/img/hero-4.jpg')"
        >
          <div
            class="container
          hero-container"
          >
            <div class="hero-content">
              <h1 class="hero-head">
                Your Vision, <br />
                <span class="hero-head-highlight">Our Tech</span>
              </h1>

              <div class="btn-container">
                <NuxtLink class="btn" to="/contact">
                  Get Started
                </NuxtLink>
                <NuxtLink class="btn transparent" to="/about">
                  Learn More
                </NuxtLink>
              </div>
            </div>
          </div>
        </SwiperSlide>
        <SwiperSlide
          class="banner"
               style="background-image:url('/img/banner-1.jpg')"

        >
          <div
            class="container
      hero-container"
          >
            <div class="hero-content">
              <h1 class="hero-head">
                Our Passion,
                <br />
                <span class="hero-head-highlight">Your Business</span>
              </h1>

              <div class="btn-container">
                <NuxtLink class="btn" to="/contact">
                  Get Started
                </NuxtLink>
                <NuxtLink class="btn transparent" to="/about">
                  Learn More
                </NuxtLink>
              </div>
            </div>
          </div>
        </SwiperSlide>
        <SwiperSlide
          class="banner"
               style="background-image:url('/img/banner-2.jpg')"

        >
          <div
            class="container
      hero-container"
          >
            <div class="hero-content">
              <h1 class="hero-head">
                Think Tech,
                <br />
                <span class="hero-head-highlight">Choose us</span>
              </h1>
              <p class="hero-para"> </p>
              <div class="btn-container">
                <NuxtLink class="btn" to="/contact">
                  Get Started
                </NuxtLink>
                <NuxtLink class="btn transparent" to="/about">
                  Learn More
                </NuxtLink>
              </div>
            </div>
          </div>
        </SwiperSlide>
  </swiper>
   </section>
</template>
<script setup>

import { Swiper, SwiperSlide } from "swiper/vue";


import "swiper/css";

// import "swiper/css/pagination";
// import "swiper/css/navigation";
import "swiper/css/effect-fade";





import { Autoplay} from "swiper";

 const modules= [Autoplay]


</script>
<style scoped>
.hero {
  height: calc(100vh - 10rem);
  margin-top: 10rem;
  width: 100%;
}
.swiper{
    height: 100%;
}

/* .hero::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--bs-overlay-black);
  opacity: 0.4;
  z-index: 1;
} */

.hero .swiper-slide.banner {
  height: 100%;
  width: 100%;

  background-position: 20% 50%;
  background-size: cover;
  background-repeat: no-repeat;
}

.hero .swiper-slide::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--bs-overlay-black);
  opacity: 0.4;
  z-index: 1;
}
.hero-container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  z-index: 22;
}
.hero-content {
  z-index: 22;
  height: 50%;
  width: 50%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
}
.hero-head {
  text-align: center;
  font-size: 6rem;
  text-transform: uppercase;

  font-weight: 800;
  color: var(--bs-white);
}

.hero-head-highlight {
  color: var(--bs-cyan);
}

/* .hero-para {
  position: relative;
  z-index: 23;
  text-align: center;
  font-size: 2.5rem;
  font-weight: 600;
  color: var(--bs-white);
} */

.btn-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.btn {
  background-color: var(--bs-cyan);
  color: var(--bs-white);
  border: none;
  padding: 1rem 2rem;
  font-size: 1.5rem;
  font-weight: 600;
  border-radius: 0.5rem;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
.btn:hover {
  background-color: transparent;
  border: 1px solid var(--bs-cyan);
}

.transparent {
  background-color: transparent;
  border: 1px solid var(--bs-cyan);
}

.transparent:hover {
  background-color: var(--bs-cyan);
}

@media (max-width: 768px) {
  .hero {
    height: calc(90vh - 10rem);
  }

  .hero-head {
    font-size: 4rem;
  }

  .hero-para {
    font-size: 1.5rem;
  }

  .btn {
    font-size: 1.5rem;
    padding: 0.5rem 1rem;
  }
}

@media (max-width: 550px) {
  .hero {
    height: calc(60vh - 10rem);
  }

  .hero-head {
    font-size: 3rem;
  }
}

@media (max-width: 400px) {
  .hero-head {
    font-size: 2rem;
  }

  .head-para {
    font-size: 1.5rem;
  }
  .btn {
    font-size: 1rem;
    padding: 1rem 1rem;
  }
}</style>
