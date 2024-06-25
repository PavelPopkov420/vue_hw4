<template>
    <div>
        <div>
        {{ product.name }}
    </div>
    <div>
        {{ formattedPrice }}
    </div>
    <div>
        
    </div>
        <template v-if="product.available">
            <span>Available</span>
        </template>
        <template v-else>               
            <span>Out of stock</span>
        </template>
    </div>
    
</template>

<script>
export default {
    name: 'ProductDetails',
    data (){
        return {
            product:{
                name: 'Ноутбук',
                price: 50000,
                available: false,        
            }
           
        }


    },
    computed:{
        formattedPrice (){
            return this.product ? `$${this.product.price}`: '';
        }
    }
}


</script>