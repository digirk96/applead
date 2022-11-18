<template>
 <footer class="footer">
      <div class="container">
        <p class="footer-content">
          &copy; <span>2022 by </span>
          <span class="highlight">AppLead</span>
        </p>
      </div>
    </footer>
</template>
<style scoped>
.footer {
  background-color: var(--bs-secondary);
  padding: 3rem 0;
}

.footer-content {
  text-align: center;
  color: var(--bs-white);
  font-size: 2rem;
}

.footer-content span {
  font-size: 1.5rem;
  margin-top: 0.5px;
}

.highlight {
  color: var(--bs-primary);
}</style>
