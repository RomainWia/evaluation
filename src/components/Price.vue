<template>
<p>{{price}}</p>

</template>

<script>
export default {
  name: 'Price',
  props: {
    msg: String
  },
  data() {
    return {
      price: '0'
    }
  },  
}
/**<select v-model="selected"> 
        <option v-for="option in options" v-bind:key="option.text" > on créé une boucle qui va tourner pour créer des option qui afficheront la valeur text du tableau de options
          {{option.text}}
        </option>
</select> */
</script>

<style scoped>

</style>

