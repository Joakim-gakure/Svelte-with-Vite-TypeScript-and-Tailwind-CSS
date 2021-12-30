<script>
    import * as animateScroll from "svelte-scrollto";
  </script>
  
  <header class="text-gray-600 body-font">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0" href="/" 
      on:click={
        () => {
          window.scrollTo({
            top:0,
            left:0,
            behavior:"smooth"
          })
        }
      }
      >       
        <h2 class="ml-3 text-xl">ABC</h2>
      </a>
      <nav class="md:mx-auto flex flex-wrap items-center justify-center">
        <a class="mr-5"
        name="navigation"
        on:click={
          () => 
            animateScroll.scrollTo({
              element:"#home",
              offset:50
            })
          
        }>Home</a>
        <a class="mr-5"  
        name="navigation"
        on:click={
          () => 
            animateScroll.scrollTo({
              element:"#services",
              offset:50
            })
          
        }>Our Services</a>
        <a class="mr-5"
        name="navigation"
        on:click={
          () => 
            animateScroll.scrollTo({
              element:"#team",
              offset:50
            })
          
        }>Our team</a>
      </nav>
    </div>
  </header>