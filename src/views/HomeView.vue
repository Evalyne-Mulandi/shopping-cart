<template>
   <main>
    <main class=" mx-auto grid grid-flow-row max-w-7xl justify-center items-center  lg:grid-cols-3 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 gap-1"> 
    <div class="flex flex-col p-2 bg-gray-300 shadow-lg shadow-black rounded-md flex-wrap gap-1 justify-center items-center mx-auto max-w-xl" v-for="c in card" :key="c">
        <h3 class="uppercase font-extrabold text-black font-mono">{{c.title}}</h3>
        <img :src="c.img" alt="" class=" w-full h-auto text-black object-cover px-1">
        <p class=" to-black">{{c.desc}}</p>
        <div class="flex flex-row   mx-auto justify gap-x-36 center items-center">
          <a href="#my-modal-2" class="btn">Info</a>

        <button class="  px-4 py-2  rounded-lg   bg-orange-500 hover:bg-orange-600 text-black"> Cart</button>
        </div>
        
    </div>
  </main>
  
<!-- Put this part before </body> tag -->
<div class="modal" id="my-modal-2">
  <div class="modal-box">
    <h3 class="font-bold text-lg">Congratulations random Internet user!</h3>
    <p class="py-4">You've been selected for a chance to get one year of subscription to use Wikipedia for free!</p>
    <div class="modal-action">
     <a href="#" class="btn">Yay!</a>
    </div>
  </div>
</div>
   </main>
</template>

 <script>
 export default {
  data(){
    return{
      card:[
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        }, {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
        {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
         {
          title:"",
          img:"https://cdn.pixabay.com/photo/2016/11/19/18/06/feet-1840619_960_720.jpg",
          desc:"shoes"
        },
       
      ]
    }
  }
 }
 </script>
