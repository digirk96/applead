<template>
    <section class="contact">
      <div class="container">
        <h3 class="contact-head">We are a full-service creative agency</h3>
        <p class="contact-text">
          Our team of designers, developers and creatives are <br />
          perfectionists who love what they do and love where they <br /> work
        </p>
        <div class="contact-wrapper">
          <div class="contact-card">
            <div class="icon">

                <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path fill="none" stroke="#000" stroke-width="2" d="M17.5,6.5 L23,9 L23,22 L16,19 L8,22 L1,19 L1,6 L6,8 M16,19 L16,12 M8,22 L8,12 M12,16.2727273 C12,16.2727273 6,11.5 6,7 C6,3.25 9,1 12,1 C15,1 18,3.25 18,7 C18,11.5 12,16.2727273 12,16.2727273 Z M13,7 C13,6.44766667 12.5523333,6 12,6 C11.4476667,6 11,6.44766667 11,7 C11,7.55233333 11.4476667,8 12,8 C12.5523333,8 13,7.55233333 13,7 Z"></path></svg>

            </div>
            <div class="detail">
              <h4>Our Locations</h4>
              <p>
                89/35 Vaish College Road,
                <br />
                Rohtak Haryana - 124001
              </p>
            </div>
          </div>
          <div class="contact-card">
            <div class="icon">
              <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M15.05 5A5 5 0 0 1 19 8.95M15.05 1A9 9 0 0 1 23 8.94m-1 7.98v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path></svg>
            </div>
            <div class="detail">
              <h4>Give Us A Call</h4>
              <p>
                +91-9711666075 <br />
                +91-9711666075
              </p>
            </div>
          </div>
          <div class="contact-card">
            <div class="icon">
             <svg stroke="currentColor" fill="currentColor" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path fill="none" stroke="#000" stroke-width="2" d="M1,4 L23,4 L23,20 L1,20 L1,4 Z M1,5 L12,13.5 L23,5"></path></svg>
            </div>
            <div class="detail">
              <h4>Help Desk</h4>
              <p>
                pulkit.goyal90@gmail.com <br />
                info@appleadtechnologies.com <br />
              </p>
            </div>
          </div>
        </div>
        <Form />
      </div>
    </section>
</template>
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
}
svg path {
    stroke-width: 2;
    stroke: var(--bs-cyan);
}
</style>
