<template>
  <img class="narrow-band-image" :src="src" ref="image" @load="startDraw" :style="imgStyle">
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true
    },
    interval: {
      type: Number,
      required: false
    },
  },
  data: function() {
    return {
      imgStyle: ""
      , intervalId: null
      , imgHeight: 0
    }
  },
  methods:{
    startDraw() {
      const dataObj = this;
      const imageObj = this.$refs.image;
      const width = imageObj.width;
      const height = imageObj.height;
      const drawInterval = !(this.interval) ? 100 : this.interval;

      this.intervalId = setInterval(()=>{
        dataObj.imgHeight += Math.floor(Math.random() * 5);
        if(dataObj.imgHeight >= height){
          dataObj.imgHeight = height;
          clearInterval(dataObj.intervalId);
        }
        dataObj.imgStyle = "display:inline;" + "width:" + width + "px;" + "height:" + dataObj.imgHeight + "px;";
      }, drawInterval);
    }
  }
}
</script>

<style scoped>

.narrow-band-image {
  display: none;
  object-fit:none;
  object-position: 0 0;
  vertical-align: top;
}
</style>
