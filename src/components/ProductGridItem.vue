<template>
<div  class="product-item" >
<img v-bind:src="product.imageUrl"/>

<h3 class="produt-name">{{product.name}}</h3>

<router-link v-bind:to="'/products/'+ product.id">
<button>view details</button>
</router-link>

</div>
</template>