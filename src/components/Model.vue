<template>
<div class="borderline" style="margin-left:0"></div>
<div class="titredimension d-flex2 margin-t f-size1">
    
    <div class="pou d-flex">
      <h2 class="f-wl m-l">2</h2>
      <h2 class="f-wl m-l">J’indique mon type de rail</h2>
    </div>
</div>
<div class="d-flex margin-t" >
  <div style="padding:20px" class="hh" >
        <label for="rail1" class="m">
            <img src="https://www.mesrideaux.fr/media/customoptions/f/o/forest_ds_s_arret_metal.jpg" alt="" style="width:100px">
            <p><span class="f-wll">Modèle DS : Fixation au plafond pour rideaux légers </span><br />(sans doublure, hauteur max 300cm)</p>
        </label>
  <input type="radio" id="rail1" name="rail" value="rail1"  class="h"/>
  </div>
  <div style="padding:20px;" class="hh">
      <label for="rail2" class="m">
          <img src="https://www.mesrideaux.fr/media/customoptions/c/s/cs_b34156.png" alt="" style="width:100px">
          <p><span class="f-wll">Modèle CS : Fixation au plafond ou au mur pour rideaux lourds </span> <br />(doublé, hauteur + 300 cm)</p>
      </label>
    <input type="radio" id="rail2" name="rail" value="rail2"  class="h" />
  </div>
   
</div>
<button v-on:click.prevent="$emit('poulet')" class="m-r bouton margin-t" style="margin-left:470px" >VALIDER</button>


</template>

<script>
export default {
  name: 'Length',
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.margin-t {
  margin-top: 2em;
}

.margin-t2 {
  margin-top: 4em;
}

.m-r {
  margin-right:0px;
}
.m-l {
  margin-left:0px;
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

.pou {
  flex-direction: row;
}

.hh {
    border: black 1px solid;
    width: 40%;
    display: flex;
    padding: auto;
    text-align: center;
}
input[type=radio]:checked+label {
	color: blue;
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
</style>
