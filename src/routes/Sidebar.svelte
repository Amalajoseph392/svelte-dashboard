
<script>






    
    let navLinks=[

    {text:'Dashboard',icon:"fa-solid fa-gauge-high",url:'/'},
    {text:'Users',icon:"fa-solid fa-user",url:'/'},

    {text:'Sign in',icon:"fa-solid fa-right-to-bracket",url:'/signin'},
    {text:'Sign up',icon:"fa-solid fa-table",url:'/signup'}
   

    ];
</script>

<main >


  

<div class='fixed  left-0 w-[250px] h-screen bg-white z-10 duration-300'>   

<nav>
    <ul class='flex flex-col p-4 text-gray-600'>
        {#each navLinks as Link}
    <li class='text-base py-3 flex cursor-pointer hover:bg-gray-200 hover:rounded-lg '>
        
        <div class="mr-4"><i class={Link.icon}></i></div>
            
            <a href={Link.url}>{Link.text}</a></li>
    {/each}
</ul>
   
    </nav>
    
    <div class="absolute top-0 left-[250px] -ml-0.5 w-0.5 h-screen bg-gray-200"></div>
  
    
    
    </div>

</main>
    
    
          
        
     