<template lang="">
    <div class="product-card">
    <div  class="product-card__title "> 
         <div>
            {{ product.name }}
         </div>
         <img
        :src="product.addedToFavourite ? '/img/star.png' : '/img/un-star.svg'"
        :alt="product.addedToFavourite ? 'Star' : 'Unstar'"
        class="favorite-icon"
        @click="toggleFavourite"
       
      >
         </div>

    <div class="product-card__body">
     <img :src="product.thumbnail" alt="">
    <p>Price : {{ product.price }}tk</p>

    </div>

       <div class="product-card__footer">
        <button @click="handleBuyClick">Buy now</button>
        <button @click="handleAddClick">Add To Cart</button>
       </div>
       
</div>
</template>
<script>
export default {
    
    props: {
        "product": {type:Object, default:() => ({}) }
    },

//     emits: {
//     'buy-now-clicked': function (eventData) {
//     if (!eventData) {
//       console.error("Data missing for buy now click event");
//       return false; 
//     }
    
//     return true; 
//    }
//   },

    methods:{
        handleBuyClick() {
            //this.$emit("buy-now-clicked");
            this.$emit("buy-now-clicked", this.product );
        },
        handleAddClick(){
            this.$emit("Add-now-clicked", this.product );
        },
        toggleFavourite(){
        this.$emit("toggle-favourite", this.product );
       // this.product.addedToFavourite = !this.product.addedToFavourite; eivhabe kora jabe na
    },
    },
    
}
</script>
<style >
.product-card{
    width: 300px;
    border: 1px solid #006f88;
    min-height: 100px;
    margin: 22px auto;
  
}
.product-card__title{
    background: #167db1;
    padding: 5px 11px;
    color: #fff;
    text-align: center;
    display: flex;
    justify-content: center;
    
}
.product-card__body{
    padding: 11px;
    text-align: center;
   
}
.product-card_body img{
    height: 111px;
    
}
.product-card__footer{
    background-color: #a3a3a3;
    padding: 5px 11px;
    text-align: center;
}
.favorite-icon {
  
  width: 15px; 
  height: 15px; 

  
}
</style>