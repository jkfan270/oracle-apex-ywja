<template>


  <div class="flex flex-col justify-center items-center space-y-0">


<div ref="vantaRef" class="w-full flex justify-center">

  <img :src="logo" class="absolute left-5 top-5 h-16 w-16 overflow: hidden;" style="width:auto;  height: 30px;">

    <div>
      <Input />
    </div>


    <div class="absolute bottom-0 right-0 h-16 w-16 ...">Scroll Down</div>


  </div>


    <div class="p-15 w-full text-center" >
      <Footer />

    </div>




</div>




</template>

<script>

import CLOUDS from 'vanta/src/vanta.clouds'
import Input from "@/components/Login/Input.vue"
import Footer from "@/components/Login/Footer.vue";
import Logo from "/src/assets/ja-solar-logo-vector.png"
//import {NWatermark} from 'naive-ui'
//import {NTable} from "naive-ui"




  export default {
  name: 'LoginPage',
    components: {
    Input,
      Footer,
      //NWatermark,
    },
  props: {
    msg: String
  },
    data:function (){
      return{
        logo:Logo
      }
    },


  mounted(){
    this.vantaEffect = CLOUDS({
      el:this.$refs.vantaRef,
      mouseControls: true,
      touchControls: true,
      gyroControls: false,
      minHeight: 950.00,
      minWidth: 1478.00,

      scale: 1.00,
      texturePath: "./gallery/noise.png"

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

