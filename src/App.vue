<template>
    <div>
      <h1>{{ msg }}</h1>

      
    <!-- <ContactDetails v-for="contact in contacts" :key="contact.name" :name="contact.name" :website="contact.website" :address="contact.address" />  -->

    <!-- <ContactDetails name="Prasanjit kumer" website="https://prasanjit.com" address="Chandpur" />  -->
      
  <!-- <PropsValidatin  name="Prasanjit kumer" website="https://prasanjit.com" address="Chandpur"/>  -->
    <!-- <PropsValidatin  name="Prasanjit kumer"  address="Chandpur"/>  -->

  <!-- <ComponentSlots ComponentSlots cardTitle="About Me" ><p>Hlw I am Prasanjit Kumer Roy, bah bah bah... </p></ComponentSlots> -->
    <!-- <ComponentSlots cardTitle="Partho Me" > 
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZbfE6B9-PCaRFHDXUtFquGzFQmflYg9AtCA&usqp=CAU" alt="">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, similique.</p>
    </ComponentSlots >
    <ComponentSlots cardTitle="Design me"> 
        <ul>
            <li>Web Dev</li>
            <li>Programing Dev</li>
            <li>Soft Dev</li>
        </ul>
    </ComponentSlots>
    <ComponentSlots  cardTitle="About Me" ></ComponentSlots> -->


    <!-- <template v-slot:default></template>  -->
    <!-- <NamedSlots cardTitle="About Me" >
     <template #default>
        <p>Hlw I am Prasanjit Kumer Roy, bah bah bah... </p>
    </template>
    <template #footer>
        <a href="https://prasanjit.com"> Learn More ...</a>
    </template>
    </NamedSlots>

    <NamedSlots cardTitle="Partho Me" > 
        <template #default>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZbfE6B9-PCaRFHDXUtFquGzFQmflYg9AtCA&usqp=CAU" alt="">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, similique.</p>
       </template>
       <template #footer>
        <button>Buy Now</button>
        <button>Add To Cart</button>
       </template>
    </NamedSlots> -->
    

    <!-- <CustomEvent 
       v-for="product in products"
      :key="product.name"
      :product="product"
      @buy-now-clicked="buyNow"
      @Add-now-clicked="addToCart"
      @toggle-favourite="handleToggle"
    > 
    </CustomEvent> -->
       
    <!-- <p>My Rating : {{ myRating }}</p>
    <TheRating v-model="myRating"> </TheRating> -->

    
   <!-- <div class="container">
    <h3>Creadit Card input</h3>
    <CreaditCard v-model:nameOnCard="nameOnCard"
                 v-model:cardNumber="cardNumber"
                 v-model:expiry="expiry"
                 v-model:cvv="cvv"
     > </CreaditCard> 
    <br>
    <hr>
    <br>
    <p>
      Name : {{ nameOnCard }} <br>
      Card Number : {{ cardNumber }} <br>
      Expire : {{ expiry }} <br>
      CVV : {{ cvv }} <br>
    </p>
 </div> -->


  <!-- <div class="container">
 <TheComment v-model="myComment" buttonText="Continue"  placeholder="Enter your comment..."   ref="nameInput" > </TheComment> 
 <br>
 <hr>  -->
 <!-- class="shadowed" eita vitore use korar jonno -->
 <!-- <br>
 <p>{{ myComment }}</p>
</div>  -->

<!-- teleport component -->
  <!-- <div class="container">
  <button @click="hide=true">Hide</button>
 <LifeCycleHook v-model="myComment" buttonText="Continue"  placeholder="Enter your comment..."  @continueClick="handleContinueClick" > </LifeCycleHook>   -->
  <!-- <br>   -->
 <!-- v-if="!hide"  -->
 <!-- class="shadowed" eita vitore use korar jonno-->
 <!-- <br>
 <p>{{ myComment }}</p>
 </div>  -->
    
 <!-- <TheDialog heading="Are you sure" v-if="showDialog" >
  <p>
    Are you really want to comment?
    <br>
    <button @click="showDialog = false">Yes</button>
    <button @click="showDialog = false">No</button>
  </p>
 </TheDialog>
 <button @click="showNotification">Show Notification</button>
  <TheNotification v-for="(n, i) in notifications" :key="i" :text="n"></TheNotification> -->
  <!-- teleport component -->

  <!-- conDetails,Login,Register -->
  <!-- <div class="container">
    <div class="tab">
      <div class="tab__menu">
        <div
          v-for="tab in tabs"
          :key="tab"
          class="tab__menu-item"
          :class="{ 'tab__menu-item--active': activeTab === tab }"
          @click="activeTab = tab"
        >
          {{ tab }}
        </div>
      </div> -->

      <!-- <div class="tab__content"> -->
        <!-- <br /> -->
        <!-- <Login v-if="activeTab === 'Login'" /> -->
        <!--  <Register v-if="activeTab === 'Register'" /> -->
        <!-- <keep-alive>
          <component :is="activeTab" />
        </keep-alive>
      </div>
    </div>
  </div> -->
    <!-- conDetails,Login,Register -->

    <div class="container">
     <h1>new user Registration</h1>
     <label >full Name</label><br>
     <!-- <input type="text" placeholder="Enter your Full name" :value="formData.fullName" @input=""> -->
     <input type="text" placeholder="Enter your Full name" v-model="formData.fullName">
     
     <!-- {{ formData }} -->
     <br>
     <label >About You</label><br>
     <textarea type="text" placeholder="Enter your Full name" v-model="formData.aboutYou" ></textarea>
     <br>
     <label><input type="radio" name="gender" value="Male" v-model="formData.gender">Male</label>
     <label><input type="radio" name="gender" class="ml-2" value="Female" v-model="formData.gender" >FeMale</label>
     <label><input type="radio" name="gender" class="ml-2" value="Other" v-model="formData.gender" >Other</label>
     <br>
     <label>Language</label>
     <br>
     <select v-model="formData.language">
      <option value="">--Select One--</option>
      <option value="Bangla">Bangla </option>
      <option value="English">English</option>
     </select>
     <br>
     <label>Skills</label>
    <br />
    <select multiple v-model="formData.skils">
      <option>HTML</option>
      <option>CSS</option>
      <option>JavaScript</option>
      <option>Python</option>
      <option>Swift</option>
    </select>
    <br>
    <label>Social Accounts</label>
    <br />
    <label><input type="checkbox" v-model="formData.socialAccounts" value="facebook" />FacebooK</label>
    <label><input type="checkbox" v-model="formData.socialAccounts" value="twitter" />Twitter</label>
    <label><input type="checkbox" v-model="formData.socialAccounts" value="lnkdien" />Linkedin</label>
    <label><input type="checkbox" v-model="formData.socialAccounts" value="instragram" />Instagra</label>
   <br />
    <label>Agreement</label><br>
    <label>
      <input type="checkbox" v-model="formData.agreed" /> I agree to the Terms
      and Services
    </label>

     
     <hr>
     <div v-for="(value, key) in formData" :key="key">
      <strong>{{ key }}:</strong>{{ value }}
    </div>
   </div>




  
  </div>
  </template>
  
  <script>
  // import ContactDetails from './ContactDetails.vue';

  // import PropsValidatin from './PropsValidatin.vue';

  // import ComponentSlots from './ComponentSlots.vue';

  // import NamedSlots from './NamedSlots.vue'

  //  import CustomEvent from './CustomEvent.vue'

  //  import TheRating  from './TheRating.vue'

  //  import CreaditCard  from './CreaditCard.vue'

  //  import TheComment  from './TheComment.vue';

  // import LifeCycleHook  from './LifeCycleHook.vue';

  // import TheDialog from './TheDialog.vue';

  // import TheNotification from './TheNotification.vue';


  //  import ConDetails from './ConDetails.vue';
  //  import Login from './Login.vue';
  //  import Register from './Register.vue';
  




  export default {
    data() {
      return {
        msg: "Welcome partho",

        // //The rating
        //  myRating:3,

        //Creadit Card
        // nameOnCard: "Mr. ",
        // cardNumber: "",
        // expiry:"",
        // cvv:"",

        // //  //The comment
        //      myComment: "Mr. ",

        // //LifeCycleHook
        //     myComment: "Mr.",
        //     // hide: false,
        //     showDialog:false,
        //     notifications: [],

        // tabs:["Login","Register","ConDetails"],
        // activeTab:"Login",
        // name:"Prasanjit Kumer Roy",
        // website:"https://parthpbd.com",
        // address:"Dhaka",

        formData:{
         fullName:"",
         aboutYou:"",
         gender:"Male",
         language:"",
         skils:[],
         agreed: false,
        socialAccounts: [],
        },



        // products:[
        // {
        //   name : "Apple iphone 12 pro",
        //   thumbnail: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZbfE6B9-PCaRFHDXUtFquGzFQmflYg9AtCA&usqp=CAU",
        //   price: "156248",
        //   addedToFavourite:true
        // },
        // {
        //   name : "Reale me",
        //   thumbnail: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZbfE6B9-PCaRFHDXUtFquGzFQmflYg9AtCA&usqp=CAU",
        //   price: "156248",
        //   addedToFavourite:false
        // },
        // {
        //   name : "Xaomi 12",
        //   thumbnail: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZbfE6B9-PCaRFHDXUtFquGzFQmflYg9AtCA&usqp=CAU",
        //   price: "156248",
        //   addedToFavourite:true
        // },
        
        // ]

   // contacts:[
        //     {
        //       name:"prasanjit kumer Roy " ,

        //       website:"https://prasanjit.com",

        //       address:"Chandpuriiii"
        //     },
        //     {
        //       name:"Partho Kumer Roy" ,
              
        //       website:"https://prasanjit.com",

        //       address:"Chandpur"
        //     },
        //     {
        //       name:"Akash Kumer Roy" ,
              
        //       website:"https://prasanjit.com",

        //       address:"Chandpuryyyy"
        //     }
        // ]
      };
    },
// mounted() {

// console.log(this.$refs.nameInput);
// },


  //   methods: {
  //   buyNow(product) {
  //       console.log("Buying......",product);
  //   },
  //   addToCart(product) {
  //       console.log("Add to cart......",product);
  //   },
  //   handleToggle(product){
  //      product.addedToFavourite = !product.addedToFavourite;
  //   },
  //  },
//   methods:{
//     handleContinueClick(){
//         this.showDialog = true; 
//     },
//     showNotification() {
//       this.notifications.push("You have a new notification");
//       setTimeout(() => {
//         this.notifications.shift();
//       },2222 );
//     },
// },
// provide(){
//     return{
//       name:this.name,
//       websiteAddress:this.website,
//       address:this.address,
//   }
// },
    components:{
    //ContactDetails,
    //PropsValidatin
    // ComponentSlots
    //  NamedSlots
    // CustomEvent
    // TheRating 
    //  CreaditCard
    // TheComment
    // LifeCycleHook,
    // TheDialog,
    // TheNotification


    
    // Login,
    // Register,
    // ConDetails,
},
// beforeCreate() {
//   console.log('beforecreate');
//   console.log(this.msg);
// },
// created(){
//   console.log('created');
//   console.log(this.msg);
// },
// beforeMount(){
//   console.log('beforeMount');
//   console.log(this.msg);
// },
// mounted(){
//   console.log('mounted');
//   console.log(this.msg);
// },
// beforeUpdate(){
//   console.log('beforUpdate');
// },
// updated(){
//   console.log('Update');
// },

};
  </script>
  
  <style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ul{
    margin-left: 22px;
  }

  body{
    font-family: sans-serif;
    line-height: 1.8;
  }
  header{
    background-color: blueviolet;
    color: aqua;
    font-size: 22px;
    padding: 22px;
  }
  header h2{
     text-align: center;
  }
  .container{
  padding: 22px;
  /* color: red;
  font-size: 33px;
  border: 3px solid green; */
  }
  button{
    margin: 5px;
    padding: 5px 11px;
    cursor: pointer;
  }
  .shadowed{
    box-shadow: 0 0 3px 2px #111;
  }
  .tab {
}

.tab__menu {
  display: flex;
}

.tab__menu-item {
  padding: 6px 15px;
  background-color: #dbdbdb;
  cursor: pointer;
}

.tab__menu-item--active {
  color: #fff;
  background-color: rgb(27, 104, 192);
}

input {
  padding: 5px 11px;
  margin-bottom: 11px;
}

textarea {
  padding: 5px 11px;
  margin-bottom: 11px;
  width: 100%;
}

.ml-2 {
  margin-left: 11px;
}
  </style>
  