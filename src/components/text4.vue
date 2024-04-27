<template>

  <form @submit.prevent="push()">

    <label for="name">Ваше имя*</label>
    <input type="text" id="name" name="name" minlength="3" placeholder="Акакий" required="true" v-model="name">

    <label for="age">Ваш возраст*</label>
    <input type="number" max="100" min="1" id="age" name="age" placeholder="18" required="true" v-model="age">

    <label for="mark">Оценка [1-10]*</label>
    <input type="number" id="mark" name="mark" min="1" max="10" placeholder="10" required="true" v-model="mark">

    <input type="image" src="src\components\imgs\butt.png">

  </form>

  <div class="alert">{{ this.alert }}</div>

  <div class="content">
    <h1>Оставленные отзывы:</h1>

    <table>
      <tr v-for="report in reports">
        <th>{{ report.name }}</th>
        <th>{{ report.age }}</th>
        <th>{{ report.mark }}</th>
      </tr>
    </table>
  </div>
</template>

<style>

table, th, td{
  border-style:dashed;
  margin-left: 5%;
  margin-right: 25%;
  width: 70%;
  text-align:center;
  border-color: gray;
  border-collapse: collapse;
}


@media (min-width: 1200px) {

  label {
    margin-left: 25%;
  }

  input[type="image"]{
    width:100px;
    height: 35px;
  }

  input {
    margin-left: 25%;
    margin-right: 25%;
    margin-top:10px;
    margin-bottom: 10px;
    width:50%;
    height: 30px;
  }
}


@media (max-width: 1200px) {

  label {
    margin-left: 10%;
  }

  input[type="image"]{
    width:65px;
    height: 30px;
  }

  input {
    margin-left: 10%;
    margin-right: 10%;
    margin-top:7px;
    margin-bottom: 7px;
    width:80%;
    height: 30px;
  }
}


@media (max-width: 800px) {

  label {
    margin-left: 7%;
  }

  input[type="image"]{
    width:65px;
    height: 30px;
  }

  input {
    margin-left: 7%;
    margin-right: 7%;
    margin-top:7px;
    margin-bottom: 7px;
    width:86%;
    height: 30px;
  }
}


@media (max-width: 550px) {

  label {
    margin-left: 5%;
  }

  input[type="image"]{
    width:65px;
    height: 30px;
  }

  input {
    margin-left: 5%;
    margin-right: 5%;
    margin-top:7px;
    margin-bottom: 7px;
    width:90%;
    height: 30px;
  }
}

</style>

<script>

  export default {
    components: {
    },

    data() {
      return {
        name:'', 
        age: null,
        mark: null,
        reports: [],
        alert:''
      }
    },

    methods: {
      push() {
        if (this.name.length>2)
          if (this.age>1 && this.age<100)
            if (this.mark > 0 && this.mark<11)
            {
              this.reports.push({
                name:this.name, 
                age:this.age, 
                mark:this.mark
              });
              this.alert= "";
              return;
            }
        this.alert= "Проверьте корректность введённых данных";
      }
    }
  } 
  
</script>