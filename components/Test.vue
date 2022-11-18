<template>
<section class="test">
    <div class="container">
        <h3 class="test-head">
            What our customers are saying about our services
        </h3>
        <p class="test-text">
            Get your company heading in the right direction with our <br />
            digital marketing strategist
        </p>
        <div class="slider">
            <Swiper
 :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :spaceBetween="30"
    :loop="true"
     :breakpoints="{
      '320': {
        slidesPerView: 1,
        spaceBetween: 20,
      },
      '768': {
        slidesPerView: 2,
        spaceBetween: 20,
      },
      '1024': {
        slidesPerView: 3,
        spaceBetween: 30,
      },
    }"
    :centeredSlides="true"  :pagination="{
      clickable: true,
    }" :navigation="false" :modules="modules" class="mySwiper">
                <SwiperSlide class="slide">
                    <div className="test-card">
                        <div className="test-img">
                            <img src='/img/wong.jpg' alt="Tset" />
                        </div>
                        <div className="text"> "AppLead is highly responsive. Thanks for the great work, I'm happy with the result. While working with the team, I found them very flexible and willing to try out various new things according to my suggestions. I am very happy with their help and I look forward to work with them on my next project."
                        </div>
                        <div className="text-name">
                            <h3>Joseph Wong</h3>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide class="slide">
                    <div className="test-card">
                        <div className="test-img">
                            <img src='/img/wong.jpg' alt="Tset" />
                        </div>
                        <div className="text"> "AppLead is highly responsive. Thanks for the great work, I'm happy with the result. While working with the team, I found them very flexible and willing to try out various new things according to my suggestions. I am very happy with their help and I look forward to work with them on my next project."
                        </div>
                        <div className="text-name">
                            <h3>Joseph Wong</h3>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide class="slide">
                    <div className="test-card">
                        <div className="test-img">
                            <img src='/img/wong.jpg' alt="Tset" />
                        </div>
                        <div className="text"> "AppLead is highly responsive. Thanks for the great work, I'm happy with the result. While working with the team, I found them very flexible and willing to try out various new things according to my suggestions. I am very happy with their help and I look forward to work with them on my next project."
                        </div>
                        <div className="text-name">
                            <h3>Joseph Wong</h3>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide class="slide">
                    <div className="test-card">
                        <div className="test-img">
                            <img src='/img/wong.jpg' alt="Tset" />
                        </div>
                        <div className="text"> "AppLead is highly responsive. Thanks for the great work, I'm happy with the result. While working with the team, I found them very flexible and willing to try out various new things according to my suggestions. I am very happy with their help and I look forward to work with them on my next project."
                        </div>
                        <div className="text-name">
                            <h3>Joseph Wong</h3>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide class="slide">
                    <div className="test-card">
                        <div className="test-img">
                            <img src='/img/wong.jpg' alt="Tset" />
                        </div>
                        <div className="text"> "AppLead is highly responsive. Thanks for the great work, I'm happy with the result. While working with the team, I found them very flexible and willing to try out various new things according to my suggestions. I am very happy with their help and I look forward to work with them on my next project."
                        </div>
                        <div className="text-name">
                            <h3>Joseph Wong</h3>
                        </div>
                    </div>
                </SwiperSlide>
            </Swiper>
        </div>
    </div>
</section>
</template>

<script setup>
import {
    Swiper,
    SwiperSlide
} from "swiper/vue";

import "swiper/css";

// import "swiper/css/pagination";
// import "swiper/css/navigation";
import "swiper/css/effect-fade";

import {
    Autoplay
} from "swiper";

const modules = [Autoplay]
</script>

<style scoped>
.test {
    padding: 6rem 0 6rem;
    width: 100%;
    height: 100%;
}

.test-head {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 4rem;
    font-weight: 600;
    color: var(--bs-black);
}

.test-text {
    text-align: center;
    font-size: 2rem;
    color: #748494;
}

.slider {
    margin: 2.5rem 0;
    width: 100%;
    height: 100%;
}

.test-card {
    width: 100%;
    height: 46rem;
    padding: 3rem;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    gap: 2rem;

    border: 1px solid #e6e6e6;
    border-radius: 5px;
}

.test-img {
    width: 8rem;
    height: 8rem;
    overflow: hidden;
    border-radius: 50%;
}

.test-img img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.text {
    font-size: 1.3rem;
    color: #748494;
    text-align: justify;
    padding: 0 1.5rem;
    line-height: 1.4;
}

.text-name h3 {
    color: var(--bs-cyan);
    margin-bottom: 1rem;
    font-size: 1.6rem;
}

.text-name p {
    color: #748494;
    font-size: 1.5rem;
}

@media (max-width: 768px) {
    .test-card {
        padding: 2rem;
        height: max-content;
    }

    .test-img {
        width: 7rem;
        height: 7rem;
    }

    .text {
        font-size: 1.5rem;
    }

    .text-name h3 {
        font-size: 1.5rem;
    }

    .text-name p {
        font-size: 1.2rem;
    }
}

/*////////////////////////////////swiper */
.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {
    height: 100%;
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */

    display: flex;

    justify-content: center;

    align-items: center;
}

.slide {
    width: 100%;
    height: 100%;
    padding: 0 1.5rem;
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.swiper-slide-active .test-card {
    background: var(--bs-cyan);
}
.swiper-slide-active .test-card .text{
    color: white;
}
.swiper-slide-active .test-card h3{
    color: white;
}
.swiper-slide-next .text {
    color:  #748494;;
}

.swiper-slide-next .text- h3 {
    color: #fff;
}

@media (max-width: 768px) {
    .test {
        padding: 3rem 0 3rem;
    }

    .test-head {
        font-size: 3rem;
    }

    .test-text {
        font-size: 1.5rem;
    }

    .swiper {
        width: 100%;
    }

    .slide {
        width: 100%;
        height: 100%;
    }
}
</style>
