<template>

  <Navigation />

  <div>
      <div class="min-h-screen bg-gray-100 page-container">

        <div class="content-wrap">
          <router-view />
        </div>

      </div>
  </div>

  <Footer />

</template>

<script lang="ts">

import Navigation from "@/components/layouts/Navigation.vue";
import Footer from "@/components/layouts/Footer.vue";

export default {
  components:{
    Navigation,
    Footer
  }
}

</script>


<style>
.page-container{
    background-color: rgba(0,0,255,0.5);
    position: relative;
    min-height: 85.2vh;
}
.content-wrap {
    padding-bottom: 5.7rem;    /* Footer height */
}
</style>