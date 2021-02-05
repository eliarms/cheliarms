<template>
 <div>
<h1>{{title}}</h1>
<div class="page-wrap">
<ProductsList :products="cartItems"/>

<button class="remove-button">Remove from cart</button>

</div>
<h3 id="total-price">Total: $ {{ totalPrice }}</h3>
<button id="checkout-button">Proceed to checkout</button>
</div>


</template>

<script>
import {cartItems} from '../fake-data';
import ProductsList from '../components/ProductsList';
export default {
    name:'CartPage',
    components: {
      ProductsList,
      },
    data(){
        return {
            cartItems,
            title:'This is a Cart Item',
        }},
        computed:{
            totalPrice(){
                return this.cartItems.reduce(
                    (sum, item)=> sum +Number(item.price),
                    0,
                );
            }
        }
    };
    

</script>

<style scoped>
  h1 {
    border-bottom: 1px solid black;
    margin: 0;
    margin-top: 16px;
    padding: 16px;
  }

  #total-price {
    padding: 16px;
    text-align: right;
  }

  #checkout-button {
    width: 100%;
  }

  
</style>