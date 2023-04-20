<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="https://vuejs.org/images/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->



  <Header :title="title" />
    <div id="inner-page" class="container mt-5 mb-5  shadow-lg bg-white border border-1 rounded">


    <div class="row mt-5 mb-5">


      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12  mt-2 mb-2 border-end orange" >
        <UserInput
            :formData="formData"
            @ChangeFormData="ChangeFormData($event)"
        />

          <br>

        <UserInputEn
                  :formDataEn="formDataEn"
                  @ChangeFormDataEn="ChangeFormDataEn($event)"
          />
      </div>

      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12  mt-2 mb-2 border-end baige ">

<GentreatedCard :empName="formData.empName" :empNameEn="formDataEn.empNameEn" />

      </div>
    </div>
  </div>




  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import UserInput from './components/UserInput.vue'
import UserInputEn from './components/UserInputEn.vue';
import GentreatedCard from './components/GentreatedCard.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    UserInput,
    UserInputEn,
    GentreatedCard
  },
  data(){
    return{
      title:"سلام - Salam",
      formData:{
        empName:""
      },
      formDataEn:{
          empNameEn:""
      }
    };
  },
  methods:{
    ChangeFormData(empName){
      console.log(empName)
      this.formData = Object.assign({},this.formData,empName)
    },
    ChangeFormDataEn(empNameEn){
        console.log(empNameEn)
        this.formDataEn = Object.assign({},this.formDataEn,empNameEn)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Tajawal', Avenir, Helvetica, Arial, sans-serif !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


#inner-page{
  background-color: #d1ccbd !important;
}

</style>
