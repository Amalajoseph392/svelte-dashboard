<script>

    let username = '';
    let email = '';
    let password = '';
    let cpassword = '';
    let regSuccess = false;
  
    function handleSubmit() {
      if (password === cpassword) {
        regSuccess = true;
        // Perform a redirect to the login page if registration is successful
        if (regSuccess) {
          window.location.href = '/login';
        }
      } else {
        alert('Passwords do not match, try again.');
      }
    }
  </script>


<div class="mx-auto md:h-screen flex flex-col justify-center items-center px-6 pt-8 pt:mt-0">
  
  
    <div class="flex items-center mt-20 ml-[-50px] md:mt-20 md:ml-[-50px] lg:mt-20 lg:ml-[-60px]">
      <img class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10" src="https://www.saashub.com/images/app/service_logos/195/kdigl8jl7ozy/large.png?1637322077" alt=""/>
      <h1 class="text-center text-lg md:text-xl lg:text-2xl font-bold text-black-800">Windster</h1>
    </div>

 
    <div class="bg-white p-8 rounded-lg shadow-md max-w-md w-full md:max-w-lg mb-[100px]">
      <h1 class="text-3xl font-semibold mb-6  text-black-700">Create a Free Account</h1>
      <form on:submit|preventDefault={handleSubmit} class="space-y-4">
        <div class="flex flex-col">
          <label for="email" class="mb-1">Your email:</label>
          <input type="text" id="email" placeholder="name@company.com" bind:value={email} class="border rounded px-3 py-2 w-full focus:outline-none focus:ring-2 focus:ring-cyan-700" required />
        </div>
  
        
  
        <div class="flex flex-col">
          <label for="password" class="mb-1">Your password:</label>
          <input type="password" id="password" placeholder="........" bind:value={password} class="border rounded px-3 py-2 w-full focus:outline-none focus:ring-2 focus:ring-cyan-700" required />
        </div>
  
        <div class="flex flex-col">
          <label for="cpassword" class="mb-1">Confirm Password:</label>
          <input type="password" id="cpassword" placeholder="........"  bind:value={cpassword} class="border rounded px-3 py-2 w-full focus:outline-none focus:ring-2 focus:ring-cyan-700" required />
        </div>

        <div class=" flex-col">
        <input type="checkbox" id="terms" name="terms" value="terms">
  <label for="terms">I accept the <span class="text-cyan-700">Terms and Conditions</span></label>

  <div class="flex flex-col mb-1 mt-4">
  
        <button type="submit" class="bg-cyan-700 text-white px-4 py-2 rounded focus:outline-none focus:ring-2 focus:ring-cyan-400 focus:ring-offset-2 w-[200px]">Create Account</button>
        </div>

        <p class="text-gray-500 mt-4">Already have an account?<a href="/signin" class="text-cyan-700">Login here</a></p>
      </form>
    </div>
</div>
  
     



     