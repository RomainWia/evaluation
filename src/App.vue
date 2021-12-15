<template>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif:wght@400;700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
<div class="major-contenant">
  <div class="left-major-contenant">
    <h1 class="margin-t f-wl">Tringle Rail</h1>
    <div id="img">
      <div v-if="image === 'image1'" >
        <img src="../img/tringles-rail.jpg" alt="" class="resize2">
      </div>
      <div v-if="image === 'image2'" >
      <img src="../img/forest_ds_s_arret_metal.jpg" alt="" class="resize2">
      </div>
    </div>
    <Image msg="" v-on:image1="image='image1'" v-on:image2="image='image2'"/>
    
  </div>
  <div class="right-major-contenant">
    <h1 class="perso-titre f-size2 margin-t2">Personnalisez votre produit :</h1>
    <div v-if="step === 'step1'">
      <Length msg="" v-on:step1="step = 'step2'" /><!-- je prends ce qui a dans ma valeur output pour la mettre dans la valeur price1 -->
    </div>
    <div v-if="step === 'step2'">
      <Model msg="" v-on:poulet="step = 'step3'" /> <!--je dois cherche le moyen d'envoyer depuis Model la valeur en fonction du choix fait, après cela je le met dans la valeur price2 et la valeur totale se calculera en fonction -->
    </div>
    <div v-if="step === 'step3'"> <!--jmême principe que l'exercice 2 -->
      <Color msg="" />
    </div>
    <Price msg="" />
  </div>
     
</div>
  
  
</template>

<script>

import Image from './components/Image.vue'
import Length from './components/Length.vue'
import Price from './components/Price.vue'
import Model from './components/Model.vue'
import Color from './components/Color.vue'

export default {
  name: 'App',
  components: {
    Image,
    Length,
    Price,
    Model,
    Color
  },

  data() {
    return {
      image:'image1',
      output:'',
      message:'',
      step: 'step1',
      price1:'',
      price2:'',
      price3:'',
      price: this.price1 + this.price2 + this.price3
      
    }
  }, 
}
</script>

<style>
  * {
    margin: 0 auto;
    font-family: Noto Serif;
  }

  .major-contenant {
    width: 70%;
    display: flex;
  }

  .left-major-contenant {
    width: 100%;
    margin: 0;
  }

  .right-major-contenant {
    width: 100%;
  }

  .f-wl {
    font-weight: 400;
  }
  .f-wll {
    font-weight: 600;
  }

  .d-flex {
    display: flex;
  }

  .resize2 {
    width: 500px;
    height: 500px;
  }

  .margin-t {
    margin-top: 1em;
  }

  .margin-t2 {
    margin-top: 3em;
  }

  .perso-titre {
    margin-top: 4em;
  }

  .borderline {
    border-top : 1px solid #000;
    width : 100%;
  }
 
  .f-size2 {
    font-size: 1.2em;
  }
</style>
