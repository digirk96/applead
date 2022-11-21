<template>
<nav class="navbar">
    <div class="container nav-container">
        <NuxtLink class="logo" to="/">
            <img src="/img/logo1.png" alt="logo" />
        </NuxtLink>

        <ul class="menu " id="menu">
            <li>
                <NuxtLink class="menu-item " to="/">
                    Home
                </NuxtLink>
            </li>
            <li>
                <NuxtLink class="menu-item" to="/about">
                    About
                </NuxtLink>
            </li>
            <li>
                <NuxtLink class="menu-item" to="/services">
                    Services
                </NuxtLink>
            </li>

            <li>
                <NuxtLink class="menu-item" to="/blogs">
                    Blogs
                </NuxtLink>
            </li>

            <li>
                <NuxtLink class="menu-item" to="/contact">
                    Contact
                </NuxtLink>
            </li>
        </ul>
       
        <div class="hambur" onclick="document.querySelector('.menu').classList.toggle('menu-active')">
            <div></div>
            <div>

            </div>
            <div>

            </div>
        </div>

    </div>

</nav>
<a href="" class="whatsapp">
    <i class="fa-brands fa-whatsapp"></i>
</a>
</template>

<script setup>

</script>
<style scoped>
.hambur {
    height: 2.5rem;padding: 3px 0;
    display: flex;
    width: 3rem;
    background-color: var(--bs-cyan);
    
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    display: none;

}
.hambur div{
  width: 80%;
  height: 2px;
  cursor: pointer;
  background-color: white;
}

.whatsapp {
    position: fixed;
    z-index: 100;
    bottom: 3rem;
    right: 3rem;
    font-size: 5rem;
    color: green;
}

.navbar {
    height: 10rem;
    width: 100%;
    position: fixed;
    background-color: var(--bs-white);
    z-index: 9999999;
    top: 0;
    left: 0;
    right: 0;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.2);
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

.logo {
    height: 5rem;
}

.logo img {
    height: 100%;

    object-fit: contain;
}

.menu {
    display: flex;

    align-items: center;
    gap: 5rem;

}



.menu-item {
    color: var(--bs-black);
    position: relative;
    font-weight: 600;
    transition: all 0.3s ease;
}

.menu-item::after {
    content: "";
    position: absolute;
    bottom: -0.5rem;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--bs-cyan);
}

.menu-item:hover::after {
    width: 100%;
}

.menu-item:hover {
    color: var(--bs-cyan);
}

.active {
    color: var(--bs-cyan);
}

.active::after {
    width: 100%;
}

.hamburger {
    display: none;
}

.line {
    width: 2.2rem;
    height: 0.3rem;
    background-color: var(--bs-cyan);
}

.line:nth-child(2) {
    width: 1.8rem;
}

.line+.line {
    margin-top: 0.3rem;
}

@media (max-width: 768px){
  .hambur{
    display: flex;
  }
  .menu{
    position: absolute;
    top:10rem;
    width: 100%;
    padding: 5rem;
    left:0;
    border-top:1px solid var(--bs-cyan);
    flex-direction: column;
    transform: translateX(-100%);
    background-color: white;
    transition: all 0.3s ease-in-out;
  }
}

.menu-active {
    
 transform: translateX(0%);
  
    transition: all 0.3s ease-in-out;
}
</style>


