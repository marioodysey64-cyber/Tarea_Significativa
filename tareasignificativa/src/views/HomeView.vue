<template>
  <div class="home">
    <NavBar/>
    <CyDComponent/>
    <FooterComponent/>
  </div>
</template>

<script>
// @ is an alias to /src
import FooterComponent from '@/components/FooterComponent.vue';
import CyDComponent from '@/components/CyDComponent.vue'
import NavBar from '@/components/NavBar.vue';

export default {
  name: 'HomeView',
  components: {
    NavBar,
    CyDComponent,
    FooterComponent
  }
}
</script>
