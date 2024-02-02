<template>
  <v-container>
    <v-row>
      <v-col>
        <SliderView />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SliderView from '@/components/SliderView.vue';

export default {
  name: 'HomeView',

  components: {
    SliderView
  },
}
</script>
