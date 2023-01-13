<template>
  <div class="container">
    <!--
    <button class="bg-red-500 hover:bg-red-700">
      Hover me
    </button>
    -->

    <div ref='vantaRef'>Foreground content here</div>

  </div>
</template>

<script>
//import * as THREE from 'three'


import CLOUDS from 'vanta/src/vanta.clouds'

  export default {
  name: 'LoginPage',
  props: {
    msg: String
  },

  mounted(){
    this.vantaEffect = CLOUDS({
      el:this.$refs.vantaRef,

    })
  },


    beforeUnmount() {
    if(this.vantaEffect){
      this.vantaEffect.destroy()
    }
    }


  }

</script>
