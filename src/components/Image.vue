<template>
<button  v-on:click.prevent="$emit('image1')"><img src="../../img/tringles-rail.jpg" alt="tringles" class="resize"></button>
<button v-on:click.prevent="$emit('image2')"><img src="../../img/forest_ds_s_arret_metal.jpg" alt="tringles2s" class="resize"></button>
</template>

<script>
export default {
  name: 'Image',
  props: {
    msg: String
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.resize {
  width: 10px;
}
</style>
