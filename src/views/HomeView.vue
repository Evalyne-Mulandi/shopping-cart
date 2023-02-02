<template>
   <main>
    <Navigation :cart="cart"/>
    <main class=" mx-auto grid grid-flow-row max-w-7xl justify-center items-center  lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 gap-1"> 
    <div class="flex flex-col p-2 bg-gray-300 shadow-lg shadow-black rounded-md flex-wrap gap-1 justify-center items-center mx-auto max-w-xl" v-for="c in card" :key="c">
        <h3 class="uppercase font-extrabold text-black font-mono"></h3>
        <img :src="c.img" alt="" class=" w-full h-auto text-black object-cover px-1">
        <p class=" to-black"> </p>
        <div class="flex flex-row   mx-auto justify gap-x-36 center items-center">
          <label for="my-modal-3" class="btn"  @click="details(c.productId)">info</label>

        <button class="  px-4 py-2  rounded-lg   bg-orange-500 hover:bg-orange-600 text-black" @click="addToCart(c.productId)"> Cart</button>
        </div>  
    </div>
  </main>
  
<input type="checkbox" id="my-modal-3" class="modal-toggle" />
<div class="modal">
  <div class="modal-box relative">
    <label for="my-modal-3" class="btn btn-sm btn-circle absolute right-2 top-2">✕</label>
    <h3 class="text-lg font-bold">{{ selectedName }}</h3>
    <p class="py-3"> {{ selectedDesc }}</p>
  </div>
</div>
  <div class="m-3 bg-slate-800 text-orange-600 text-sm py-4">copyright &copy; 2023  shopping cart </div>
   </main>
</template>

 <script>
 import Navigation from '@/components/Navigation.vue'
 export default {
  components:{
Navigation
  },
  data(){
    return{
      card:[
        {
          productId:"1",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:" nike canvas shoes size 38",
          price: 20,
          color:"black"
        },
        {
          productId:"2",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 43",
          price: 20,
          color:"black"
        },
        {
          productId:"3",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 45",
          price: 20,
          color:"black"
        },
        {
          productId:"4",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 50",
          price: 20,
          color:"black"
        },
        {
          productId:"5",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 64",
          price: 20,
          color:"purple"
        },
        {
          productId:"6",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 24",
          price: 20,
          color:"violet"
        }, {
          productId:"7",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 76",
          price: 20,
          color:"yellow"
        },
        {
          productId:"8",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 36",
          price: 20,
          color:"red"
        },
         {
          productId:"9",
          name:"canvas",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"nike canvas shoes size 43",
          price: 20,
          color:"white"
        },
       
      ],
      selectedProduct:'',
      selectedPrice:'',
      selectedName:'',
      selectedDesc:'',
      image:'',
      cart:[]
    }
  },
  methods:{
    details(id){
      let newId = this.card.filter((i) => {
        /*  this.selectedProduct = this.selectedProduct + newId.name;
          this.selectedPrice = this.selectedPrice + newId.price;
          console.log(this.selectedPrice);
          console.log(this.selectedProduct); */
        return i.productId === id;})
        this.selectedProduct = this.selectedProduct + newId[0].name;
      this.selectedPrice = this.selectedPrice + newId[0].price;
      this.selectedName = this.selectedName + newId[0].name;
      this.selectedDesc = this.selectedDesc + newId[0].desc;
  console.log(newId);
    },
    addToCart(id){
      let newId = this.card.filter((i) => {
        /*  this.selectedProduct = this.selectedProduct + newId.name;
          this.selectedPrice = this.selectedPrice + newId.price;
          console.log(this.selectedPrice);
          console.log(this.selectedProduct); */
        return i.productId === id;})
        
      this.selectedPrice = this.selectedPrice + newId[0].price;
      this.selectedName = this.selectedName + newId[0].name;
      this.image = this.image + newId[0].img;
      this.cart.push(newId[0]);
  console.log(this.cart);
    }
  }
 }
 </script>
