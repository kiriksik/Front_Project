<template>
  <div class="header">
    <nav>
      <a id="link1" @click="change1()">Главная страница</a>
      <a id="link2" @click="change2()">О нас</a>
      <a id="link3" @click="change3()">Товары</a>
      <a id="link4" @click="change4()">Оставить отзыв</a>
    </nav>
  </div>

  <div class="content">
    <text1 v-if="this.main ===1"/>
    <text2 v-if="this.main ===2"/>
    <text3 v-if="this.main ===3"/>
    <text4 v-if="this.main ===4"/>
  </div>

</template>

<style scoped>


@media (min-width: 1200px){
  .header{
    font-size: 30px;
  }
  .content{
    padding-top: 120px;
    margin-bottom: 40px;
    font-size: 15px;
  }
}
@media(max-width: 1200px){

  .header{
    font-size: 25px;
  }

  .content{
    padding-top: 120px;
    margin-bottom: 40px;
    font-size: 20px;
  }
}
@media(max-width: 800px){
  .header{
    font-size: 25px;
  }

  .content{
    padding-top: 120px;
    margin-bottom: 40px;
    font-size: 25px;
  }
}
@media(max-width: 550px){
  .header{
    font-size: 20px;
  }

  .content{
    padding-top: 120px;
    margin-bottom: 40px;
    font-size: 30px;
  }
}

.header {
  width: 100%;
  height: 100px;
  background-color: #3498db;
  text-align: center;
  position: relative;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  overflow: hidden;
  

  nav {
    position: absolute;
    bottom: 0;
    height: 60px;
    line-height: 60px;
    width: 100%;
    background-color: rgba(0,0,0,.1);
    a
    {
      color: #fff;
      display: inline-block;
      padding: 10px 15px;
      line-height: 1;
      text-decoration: none;

      
        &:hover
        {
          color: black;
        }
    }
  }
}

p
{
  margin-bottom: 2rem;
  line-height: 2;
  color: #7f8c8d;
}

.wrapper
{
  width: 800px;
  margin: 0 auto;
}

</style>

<script>
  import text1 from './components/text1.vue';
  import text2 from './components/text2.vue';
  import text3 from './components/text3.vue';
  import text4 from './components/text4.vue';


  export default {
    components: {
      text1, 
      text2,
      text3,
      text4
      
  },
    data() {
      return {
        main: 1
      }

    },
    methods: {

      change1() {
        this.main=1;
        
      },

      change2() {
        this.main=2;
        
      },

      change3() {
        this.main=3;
      },

      change4() {
        this.main=4;
      }
    }
  }

</script>