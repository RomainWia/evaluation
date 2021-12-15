<template>
<div class="borderline" style="margin-left:0"></div>
<div class="titredimension d-flex2 margin-t f-size1">
    
    <div class="pou d-flex" style="margin-left:0px">
      <h2 class="f-wl m-l">1</h2>
      <h2 class="f-wl m-l" style="margin-left:10px">J’indique mes dimensions</h2>
    </div>
</div>
<div >
  <form class="dimension-input margin-t d-flex2">
    <label for="dimension" class="m-l " >Longueur du rail :</label>
    <input type="number" name="date" id="number" min="0" max="200" ref="my_input" class="m-l margin-ts ppp"  placeholder="min 0cm/ max 200cm" required />
    <button @click.prevent="getFormValues()" @click="emitCustomEvent" v-on:click.prevent="$emit('step1')" class="m-r bouton margin-ts" >VALIDER</button>
</form>
</div>



</template>

<script>
export default {
  name: 'Length',
  props: {
    msg: String
  },
  data() {
    return {
      output:''
    }
  },  
  
  methods: {
    getFormValues () {
      this.output = this.$refs.my_input.value
    },

    emitCustomEvent() {
            this.$emit('price-actu', { output: '' })
        }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.margin-t {
  margin-top: 2em;
}
.margin-ts {
  margin-top: 1em;
}

.margin-t2 {
  margin-top: 4em;
}

.f-size1 {
  font-size: 0.8em;
}

.d-flex2 {
  display: flex;
  flex-direction: column;
}

.m-l {
  margin-left:0px;
}
.m-r {
  margin-right:0px;
}

.pou {
  flex-direction: row;
}

.bouton {
  border: none;
  background-color: rgb(29, 29, 117);
  color: white;
  padding-left: 25px;
  padding-right: 25px;
  padding-top: 10px;
  padding-bottom: 10px;
}

.ppp {
  width: 200px;
  height: 50px;
}
</style>
