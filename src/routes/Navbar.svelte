<script>

import {onMount} from "svelte";
import Sidebar from "./Sidebar.svelte";
let isOpen=false; 

onMount(() => {
    if (window.innerWidth >= 768) {
      isOpen = true;
    }
  });



    

</script>
<main>
    <div class="bg-white mt-[-21px] pt-4">
    <div class='Max-w-[1800px px-4 pb-4 items-center'>
        <div class='  px-4 items center mt-5'>
        <div class='  flex justify-start '>
        
        
        
            <div class=' flex items-center  px-4  justify-start '>
                
                
                <button class="cursor pointer mr-4 lg:hidden">
                    <i class="fa-solid fa-bars"></i></button>

                   
      
      
        <img class='max-w-[25px]'src= "https://www.saashub.com/images/app/service_logos/195/kdigl8jl7ozy/large.png?1637322077" alt=""/>
        <h1 class='text-2xl font-bold sm:text-2xl lg:text-2xl px-2 '>Windster</h1>
        
        
        
  
        
        
       
        
        
        <div class=' bg-gray-100  hidden md:flex items-center py-1 ml-[100px] w-[60px] h-[40px] sm-w-[200px] pb-px lg:w-[250px] rounded-lg border border-black-100'>
  <input class="bg-gray-100 outline-none"type="text" placeholder='Search'>
        </div>
        
        </div>
        
        
        
        
        
        
        
        
        
        
        <div class='flex md:flex md:flex-grow flex-row justify-end space-x-5 items-center'>
        <div>
        <h1 class='hidden lg:flex '>Open Source ❤️ </h1>
        </div>
      
        <div class='hidden lg:flex items-center  text-[14px] border border-black-100 rounded-lg'>
        
        
        <div class='bg-gray-200 text-black hidden md:flex items-center'>Star</div>
        
        
        
        
        <p class='p-2'>776</p>
        </div>
        
        
        <button class=' bg-cyan-700 text-white hidden md:flex items-center py-2 mx-4 rounded-lg w-[120px]'>
    Upgrade to Pro
        </button>
        </div>


        
        </div>
        
        
    
</main>




<hr>

{#if isOpen}
<Sidebar/>

{/if}


<style>
    i{
        size: 20px;
    }
</style>