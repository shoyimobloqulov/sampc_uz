<script>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue';

export default {
  components: {
    Navbar
  },
}

</script>

<template>
  <div id="app" class="font-roboto bg-gray-100">
    <Navbar />
  </div>

  <RouterView />
</template>

<style>
@import "assets/css/app.css";

::-webkit-scrollbar {
  width: 5px;
}

::-webkit-scrollbar-track {
  background: #2D3748;
}

::-webkit-scrollbar-thumb {
  background: #CBD5E0;
}

::-webkit-scrollbar-thumb:hover {
  background: #2D3748;
}
</style>
