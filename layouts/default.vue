<template>
  <div>

    <AppHeader />
    <slot />
    <AppFooter />
  </div>
</template>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Mulish:wght@200;300;400;500;600;700;800;900&display=swap");
:root {
  --bs-blue: #0d6efd;
  --bs-indigo: #6610f2;
  --bs-purple: #6f42c1;
  --bs-pink: #d63384;
  --bs-red: #dc3545;
  --bs-orange: #fd7e14;
  --bs-yellow: #ffc107;
  --bs-green: #198754;
  --bs-teal: #20c997;
  --bs-cyan: #0dcaf0;
  --bs-gray: #cacaca;
  --bs-gray-dark: #343a40;
  --bs-primary: #1292ee;
  --bs-secondary: #000;
  --bs-success: green;
  --bs-info: #ff0;
  --bs-warning: #ff0;
  --bs-danger: red;
  --bs-light: #fff;
  --bs-dark: #000;
  --bs-white-gray: #f2f2f2;
  --bs-white-opacity-50: hsla(0, 0%, 100%, 0.5);
  --bs-white: #fff;
  --bs-overlay-black: #030f27;
  --bs-font-sans-serif: system-ui, -apple-system, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  --bs-font-monospace: SFMono-Regular, Menlo, Monaco, Consolas,
    "Liberation Mono", "Courier New", monospace;
  --bs-gradient: linear-gradient(
    180deg,
    hsla(0, 0%, 100%, 0.15),
    hsla(0, 0%, 100%, 0)
  );
}

* {
  user-select: none;
}

*,
*::before,
*::after {
  margin: 0;
  padding: 0;

  box-sizing: border-box;
}
html {
  font-size: 62.5%;
  scroll-behavior: smooth;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: normal;
}

a {
  text-decoration: none;
  color: var(--black);
}


.para ul{
  list-style-type:  disc !important;
  
}
li{
  list-style: none;
}

.para ul li{
  list-style:disc;
  margin-left: 1.5rem;
  
}
body {
  font-family: "Mulish", sans-serif;
  font-size: 1.6rem;
  overflow-x: hidden;
}

.container {
  max-width: 120rem;
  width: 100%;
  margin: 0 auto;
}

@media (max-width: 1200px) {
  .container {
    width: 90%;
  }
}</style>
