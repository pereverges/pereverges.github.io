<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="CheckInAlert" />
    </div>
  </header>
  <div class="footer">
    © {{ new Date().getFullYear() }} Whitecap Associates, LLC
  </div>
</template>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.footer {
  text-align: center;
  padding: 10px;
  background-color: #f8f9fa;
  color: #333;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
