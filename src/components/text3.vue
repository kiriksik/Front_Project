<template>

    <div class="slaider">
      xd
      <img class="slide-image" :src="getImgUrl(images[0])">
    </div>
  
</template>


<style>
  .slaider {
    margin-left:10%;
    margin-right: 10%;
  }
</style>

<script>

    export default{
    data(){
        return {
            images: [
                "/imgs/img1.png",
                "/imgs/img2.png",
                "/imgs/img3.png",
                "/imgs/img4.png",
                "/imgs/img5.png"
            ]
        }
    },
    mounted(){
        window.setInterval(()=>{
            this.slide();
        }, 5000);
    },
    methods: {
        getImgUrl(im) {
            return require('../assets' + im)
        },
        slide(){
            let first = this.images.shift();
            this.images = this.images.concat(first);
        },
    }
    }
</script>
