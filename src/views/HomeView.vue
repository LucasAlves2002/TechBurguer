<template>

  <v-container>
    <SideBar/>
    <v-row>
      <v-col>
        <SliderView />
      </v-col>

    </v-row>
    
  </v-container>
  
</template>

<script>
import SliderView from '@/components/SliderView.vue';
import SideBar from '../components/SideBar.vue'

export default {
  name: 'HomeView',

  components: {
    SliderView,
    SideBar
  },
}
</script>
<style scoped>
.button{
    background-color: orange !important;
    color: white !important;
    height: 36px !important;
    min-width: 64px !important;
    padding: 0 16px !important;
  }
</style>
