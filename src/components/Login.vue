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
import * as THREE from 'three'
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

    CLOUDS({
      el: this.$refs.vantaRef,
      mouseControls: true,
      touchControls: true,
      gyroControls: false,
      minHeight: 200.00,
      minWidth: 200.00,
      scale: 1.00,
      scaleMobile: 1.00,
      color: 0xdec790,
      backgroundColor: 0xc04393,
      spacing: 12.00

    }),

    beforeUnmount() {
    if(this.vantaEffect){
      this.vantaEffect.destroy()
    }
    }


  }

</script>
