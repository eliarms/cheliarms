<template>

<div  class="product-container" >
<img clas="product-image" :src="product.imageUrl"/>
<div class="details-wrap">
<h3>{{product.name}}</h3>
<h3>${{product.price}}</h3>
</div>
</div>
</template>
<script>
export default {
    name: 'ProductListItem',
    props:['product']
}
</script>
<style scoped>
.product-container {
    align-content: 'center';
    border-bottom: 1px solid #ddd;
    display: flex;
    padding: 16px;
    width: 100%;
  }

  .product-image {
    flex: 1;
    height: 100px;
    max-width: 100px;
  }

  .details-wrap {
    padding: 0 16px;
    flex: 3;
  }

  .remove-button {
    flex: 1;
    margin: auto;
  }
</style>