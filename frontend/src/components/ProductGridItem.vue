<template>
<div  class="product-item" >
<img v-bind:src="product.imageUrl"/>

<h3 class="produt-name">{{product.name}}</h3>

<router-link v-bind:to="'/products/'+ product.id">
<button>view details</button>
</router-link>

</div>
</template>
<script>
export default {
    name: 'ProductGridItem',
    props: ['product'],
}
</script>
<style scoped>
.product-item {
    align-items: center;
    border-radius: 8px;
    box-shadow: 0px 2px 5px #888;
    display: flex;
    flex-direction: column;
    margin-bottom: 2%;
    padding: 20px;
    position: relative;
    width: 32%;
  }

  .product-name {
    margin-bottom: 0;
  }

  img {
    height: 200px;
    width: 200px;
  }

  a {
    width: 100%;
  }

  button {
    width: 100%;
  }
</style>