<template>
  <img class="nbi" :src="src" ref="image" @load="startDraw" :style="imgStyle">
</template>

<script>
export default {
  props: {
    src: String,
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

      this.intervalId = setInterval(()=>{
        dataObj.imgHeight += Math.floor(Math.random() * 5);
        if(dataObj.imgHeight >= height){
          dataObj.imgHeight = height;
          clearInterval(dataObj.intervalId);
        }
        dataObj.imgStyle = "display:inline;" + "width:" + width + "px;" + "height:" + dataObj.imgHeight + "px;";
      }, 100);
    }
  }
}
</script>

<style scoped>

.nbi {
  display: none;
  object-fit:none;
  object-position: 0 0;
  vertical-align: top;
}
</style>
