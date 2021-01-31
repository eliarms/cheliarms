<template>
<div>
<h1>{{title}}</h1>
<div class="page-wrap">

<ProductsGrid :products="products"/>
</div>
</div>
    
</template>

<script>
import {products} from '../fake-data';
import ProductsGrid from '../components/ProductGrid';
export default {
    
    name:'ProductsPage',
    components:{
      ProductsGrid,
    },
    data(){
        return {
            title:'hello',
            products
        };
    }
    
};
</script>