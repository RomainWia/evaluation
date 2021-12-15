<template>
<div class="borderline" style="margin-left:0"></div>
<div class="titredimension d-flex2 margin-t f-size1">
    
    <div class="pou d-flex m-l">
      <h2 class="f-wl m-l">3</h2>
      <h2 class="f-wl m-l" style="margin-left:10px">Je séléctionne ma couleur</h2>
    </div>
</div>
<div class="d-flex margin-t" >
  <div style="padding:20px" class="hh" >
        <label for="color1" class="m">
          <div style="background-color: white; width:200px; height:100px;border: black 1px solid;"></div>
          <p><span class="f-wll">Blanc </span></p>
      </label>
    <input type="radio" id="color1" name="color" value="color1"  class="h" />
  </div>
  <div style="padding:20px;" class="hh">
      <label for="color2" class="m">
          <div style="background-color: black; width:200px; height:100px"></div>
          <p><span class="f-wll">Noire </span></p>
      </label>
    <input type="radio" id="color2" name="color" value="color2"  class="h" />
      
  </div>
   
</div>
<button class="m-r bouton margin-t" style="margin-left:470px">Valider</button>


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
