<script>
import ImageSlider from './components/image-slider/image-slider.vue';

export default {
    components:{
      ImageSlider
    }
  };
</script>
<style>
html,body { 
  width:100%;
  height:100%;
  margin:0;
  padding:0;
}

body { 
  box-sizing:border-box;
  padding: 20px;
}
.image-slider{
  height: 300px;
}
</style> 





<template>
  <body>
    Application started
    <image-slider />
  </body>
</template>