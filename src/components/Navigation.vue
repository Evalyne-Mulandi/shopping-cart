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
    <a href="#my-modal-2" class="btn btn-accent">your cart </a>
  </nav>
<!-- Put this part before </body> tag -->
<div class="modal" id="my-modal-2">
  <div class="modal-box">
    <h3 class="font-bold text-lg">shop with us</h3>
    <p class="py-4"> your cart is empty please select an item</p>
    <div class="modal-action">
     <a href="#" class="btn">login to proceed</a>
    </div>
  </div>
</div>
</template>

<script>
export default {

}
</script>

<style>

</style>