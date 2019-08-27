<template>
  <div class="nbi">
    <img :src="src" ref="image" @load="startDraw" :style="imgStyle">
    <p>test</p>
  </div>
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
    startDraw(event) {
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
        dataObj.imgStyle = "width:" + width + "px;" + "height:" + dataObj.imgHeight + "px;";
      }, 100);
    }
  },
  created: function() {
  }
}
</script>

<style scoped>
.nbi {
}

.nbi > img {
  object-fit:none;
  object-position: 0 0;
}
</style>
