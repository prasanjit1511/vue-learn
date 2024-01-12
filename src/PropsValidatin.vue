<template>
    <div class="contact-details">
      <h1 class="contact-heading">props validation</h1>
      <p><strong>Name:</strong>{{ name }}</p>
      <p><strong>Website:</strong> {{ website }}</p>
      <p><strong>Address:</strong> {{ address }}</p>
      
    </div>
  </template>
  
  <script>
  export default {
      // props:["name" ,"website","address"],
      props:{
        // name: String,
        name: {
          type: String,
        //   validator:function(){

        //   }
        },
        website:{
          type: String,
          required: false,
            default:"https://prasanjit.com",
          
        },
        address: {
            type: String,
            required: true,
           
        }
      },
    data(){
      return {
        
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-details{
    border: 1px solid gray;
    margin: 11px 22px;
    padding: 22px;
  }

  .contact-heading{
    background-color: palegreen;
  }
  </style>
  