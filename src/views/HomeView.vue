<template>
<v-app>
 <the-navbar class="index" />
 <the-dashboard />
 <the-footer />
</v-app>
 
</template>

<script>
  import TheNavbar from '../components/TheNavbar.vue'
import TheDashboard from '@/components/TheDashboard.vue'
import TheFooter from '@/components/TheFooter.vue'

  export default {
    name: 'HomeD',

    components: {TheNavbar,TheDashboard,TheFooter},
  }
</script>

<style scoped>
.index{
z-index: 9999;
}

</style>
