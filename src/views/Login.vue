<template>


  <div class="flex flex-col justify-center items-center space-y-0">


<div ref="vantaRef" class="w-full flex justify-center">

  <!--
  <img :src="logo" class="absolute left-5 top-5 h-9 w-auto overflow: hidden;" >
-->
  <h6 class="text-white text-xl font-bold absolute shadow-sm left-5 top-5 w-auto overflow: hidden;">JASolar Oracle APEX</h6>
    <div>
      <Input />
    </div>


    <div class="absolute bottom-5 right-5 h-12 w-12" >
      <n-icon size="50" color="#a3e635">
        <svg class="animate-bounce" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 12 12"><g fill="none"><path d="M6 1a5 5 0 1 1 0 10A5 5 0 0 1 6 1zm1.854 4.854a.5.5 0 1 0-.708-.708L6 6.293L4.854 5.146a.5.5 0 1 0-.708.708l1.5 1.5a.5.5 0 0 0 .708 0l1.5-1.5z" fill="currentColor"></path></g></svg>
      </n-icon>



    </div>


  </div>


    <div class="p-15 w-full text-center" >
      <Footer />

    </div>




</div>




</template>

<script>

import NET from 'vanta/src/vanta.globe'
import Input from "@/components/Login/Input.vue"
import Footer from "@/components/Login/Footer.vue";
import Logo from "/src/assets/ja-solar-logo-vector.png"
import {NIcon} from "naive-ui"
//import {NWatermark} from 'naive-ui'
//import {NTable} from "naive-ui"




  export default {
  name: 'LoginPage',
    components: {
    Input,
      Footer,
      NIcon,
      //dropdown,
      //NWatermark,
    },
  props: {
    msg: String
  },
    data:function (){
      return{
        logo:Logo,
      }
    },


  mounted(){
    this.vantaEffect = NET({
      el:this.$refs.vantaRef,
      mouseControls: true,
      touchControls: true,
      gyroControls: false,
      minHeight: 200.00,
      minWidth: 200.00,
      scale: 1.00,
      scaleMobile: 1.00,
      backgroundColor: 0x8081e
    })
  },

    beforeUnmount() {
    if(this.vantaEffect){
      this.vantaEffect.destroy()
    }
    }


  }

</script>

<style>

</style>

