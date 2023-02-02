<template>
  <nav class="  text-lg  bg-slate-800 flex flex-row justify-around mx-auto gap-x-28">
   <div class="rounded-md ring-white">

    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
  <path fill-rule="evenodd" d="M3 6.75A.75.75 0 013.75 6h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 6.75zM3 12a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 12zm0 5.25a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75a.75.75 0 01-.75-.75z" clip-rule="evenodd" />
</svg>


   </div>

    <div>
       
      <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/blog">blog</router-link>  |
    <router-link to="/call">call us</router-link>
    </div>
    <a href="#my-modal-2" class="btn btn-accent">your cart {{ cart.length }} </a>
  </nav>
<!-- Put this part before </body> tag -->
<div class=" " v-for="item in cart" :key="item">
<div class="modal" id="my-modal-2">
  <div class="modal-box">
    <div
      class="mt-6 grid grid-cols-2 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
            >
              <div
                v-for="item in cart"
                :key="item.id"
                class="ring-1 p-1 md:p-0 md:gap-y-3 md:py-2  rounded ring-orange-600 flex justify-center items-center flex-col gap-y-2"
              >
                <div
                  class="min-h-80 aspect-w-1 aspect-h-1 w-full overflow-hidden rounded-md lg:aspect-none lg:h-20"
                >
                  <img
                    :src="item.img"
                    alt=""
                    class="h-30 w-30 object-cover object-center rounded"
                  />
                </div>
                <div class="flex justify-between">
                  <div>
                    <h3 class="text-sm text-black">
                      <a>
                        <span aria-hidden="true" class="" />
                        {{ item.name.slice(0, 5) }}..
                      </a>
                    </h3>
                  </div>
                  <p class="text-sm font-medium text-black">USD.{{ item.price }}</p>
                </div>
                
              </div>
            </div>
            <a href="https://www.paypal.com/signin" class="btn m-3  font-bold text-orange-600">Login to purchase</a>
    <div class="modal-action">
     <a href="" class="btn">close</a>
    </div>
  </div>
</div>
</div>



</template>

<script>


export default {
  props:['cart']

}
</script>

<style>

</style>