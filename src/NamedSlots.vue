<template lang="">
    <div class="the-card">
    <div  class="the-card__title ">
       {{ cardTitle }}
    </div>
    <div class="the-card__body">
       <slot>The deafult card slot </slot>

    </div>

       <div class="the-card__footer">
        <slot name="footer" v-if="$slots.footer">  
            Default footer
        </slot>
       </div>
       
</div>
</template>
<script>
export default {
    mounted(){
       console.log(this.$slots.footer)
    },
    props: ["cardTitle"]
}
</script>
<style >
.the-card{
    width: 300px;
    border: 1px solid #006f88;
    min-height: 100px;
    margin: 22px auto;
  
}
.the-card__title{
    background: #167db1;
    padding: 5px 11px;
    color: #fff;
    
}
.the-card__body{
    padding: 11px;
   
}
.the-card_body img{
    height: 111px;
    
}
.the-card__footer{
    background-color: #a3a3a3;
    padding: 5px 11px;
    text-align: center;
}
</style>