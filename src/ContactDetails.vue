<template>
    <div class="contact-details">
      <h1 class="contact-heading">props</h1>
      <p><strong>Name:</strong>{{ name }}</p>
      <p><strong>Website:</strong> {{ website }}</p>
      <p><strong>Address:</strong> {{ address }}</p>
      
    </div>
  </template>
  
  <script>
  export default {
      
        props:["name" ,"website","address"],
    data(){
      return {
        // name :"Prasanjit Kumer roy",
        // website:"https://prasanjit.com",
        // address:"Dhaka",
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
  