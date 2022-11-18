<template>
<div class="about">
      <div class="container about-container">
        <h3 class="about-head">We are a full-service creative agency</h3>
        <p class="about-text">
          Our team of designers, developers and creatives are <br />
          perfectionists who love what they do and love
        </p>

        <div class="about-content">
          <div class="about-content-left">
            <div class="img-wrap">
              <div class=" first">
                <img src='/img/about-1.jpg' alt="About" />
              </div>
              <div class=" second">
                <img src='/img/about-2.jpg' alt="About" />
              </div>
              <div class=" third">
                <img src='/img/about-shape-1.png' alt="" />
              </div>
            </div>
          </div>
          <div class="about-content-right">
            <h2 class="r-head">Every day brings new challenges</h2>
            <h4 class="r-sub-head">
              Creative agency focused on <br /> vision, product and people
            </h4>
            <p class="about-para">
              AppLead Technologies is a fast growing mobile app development
              company at the helm of latest technology breakthroughs and led by
              a competent technical team. We haven’t earned our reputation
              overnight as a leading blockchain app development company, IoT
              solutions company and Artificial Intelligence Service company.
            </p>
            <p class="about-para">
              It has been a result of consistent efforts to remain ahead of the
              technology curve and adapt to evolving app development strategies
              and services. We are a complete service provider offering flexible
              engagement models that suit every business need and budget.
              Consultation, designing, development, implementation, support, and
              marketing- we provide superior services to suit your business
              objective.
            </p>

             <NuxtLink class="btn" to="/about">
                  Read More
                </NuxtLink>



          </div>
        </div>
      </div>
    </div>
</template>

<script>

</script>

<style scoped>
.about {
  padding: 6rem 0 0;

  width: 100%;
  height: 100%;
}

.about-head {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 4rem;
  font-weight: 600;
  color: var(--bs-black);
}

.about-text {
  text-align: center;
  font-size: 2rem;
  color: #748494;
}

.about-content {
  height: 70rem;
  width: 100%;
  padding: 3rem 0;
  display: flex;
}

.about-content-left {
  width: 60%;
  padding: 3rem;
}

.img-wrap {
  width: 100%;
  height: 100%;
  position: relative;
}

.first {
  width: 40rem;
  height: 40rem;
  position: absolute;
  top: 0;
  right: 0;
  overflow: hidden;
  border-radius: 10px;
  z-index: 22;
}

.first img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}
.btn {
  background-color: var(--bs-cyan);
  color: var(--bs-white);
  border: none;
  padding: 1rem 2rem;
  width: fit-content;
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
.second {
  height: 40rem;
  width: 40rem;
  position: absolute;
  bottom: 0;
  left: 0;
  overflow: hidden;
  border-radius: 10px;
}

.second img {
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.about-content-right {
  padding: 3rem;
  width: 40%;
  height: 100%;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
.r-head {
  text-align: center;
  color: #748494;
  font-size: 2rem;
  position: relative;
}

.r-head::after {
  content: "";
  position: absolute;
  bottom: -0.3rem;
  left: 0;
  width: 5rem;
  height: 2.5px;
  background-color: var(--bs-cyan);
  transition: width 0.3s ease-in-out;
}

.r-sub-head {
  color: var(--bs-black);
  font-weight: 600;
  font-size: 3rem;
  position: relative;
}

.about-para {
  color: #748494;
  font-size: 1.6rem;
  line-height: 2.5rem;
  word-spacing: 2px;
  font-weight: 500;
}

.about-btn {
  width: max-content;
  background-color: var(--bs-cyan);
  color: var(--bs-white);
  font-size: 1.6rem;
  font-weight: 600;
  padding: 1rem 2rem;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.about-btn:hover {
  background-color: var(--bs-white);
  color: var(--bs-cyan);
  border: 1px solid var(--bs-cyan);
}

@media (max-width: 1200px) {
  .about-content {
    height: 60rem;
  }
  .about-content-left {
    width: 50%;
  }
  .about-content-right {
    width: 50%;
  }

  .first {
    width: 35rem;
    height: 35rem;
  }

  .second {
    width: 35rem;
    height: 35rem;
  }
}

@media (max-width: 768px) {
  .about-head {
    font-size: 3rem;
  }

  .about-text {
    font-size: 1.6rem;
  }
  .about-content {
    flex-direction: column;

    height: 100%;
  }
  .about-content-left {
    width: 100%;
    padding: 2rem;
  }
  .about-content-right {
    width: 100%;
    padding: 2rem;
  }

  .first {
    position: initial;
    width: 40rem;
    height: 40rem;
    margin: 0 auto;
  }

  .second {
    display: none;
  }
  .third {
    display: none;
  }

  .about-para {
    font-size: 1.5rem;
  }

  .about-btn {
    font-size: 1.5rem;
    padding: 0.5rem 1rem;
  }
}

@media (max-width: 450px) {
  .about-content-left {
    width: 100%;
    padding: 2rem;
  }
  .about-content-right {
    width: 100%;
    padding: 2rem;
  }

  .first {
    height: 30rem;
    width: 30rem;
  }

  .about-para {
    font-size: 1.3rem;
  }

  .about-btn {
    font-size: 1.3rem;
    padding: 0.5rem 1rem;
  }
}
</style>
