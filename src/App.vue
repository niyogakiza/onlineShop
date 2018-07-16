<template>
  <router-view :products="theProducts" title="Shop our award-winning product line"></router-view>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      theProducts: []
    };
  },
  created() {
    $.getJSON('https://hplussport.com/api/products')
      .done(data => { this.theProducts = data;});
  }
}
</script>


