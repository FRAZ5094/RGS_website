<script lang="ts">
  let isOpen=true;

</script>

<nav class="flex flex-row justify-between bg-primary">
  <div class="p-2 w-1/4">
      <a class="" href="#">
        <img class="w-20 md:w-full" src="/images/RGS_logo.png" />
      </a>
    </div>
  <ul class="md:inline-flex hidden flex items-center flex-col md:flex-row px-2">
    <li><a class="hover:text-red-300 border-2 text-2xl mx-4 p-4" href="#">Home</a></li>
    <li><a class="hover:text-red-300 border-2 text-2xl mx-4 p-4" href="#">Shop</a></li>
    <li><a class="hover:text-red-300 border-2 text-2xl mx-4 p-4" href="#">About</a></li>
    <li><a class="hover:text-red-300 border-2 text-2xl mx-4 p-4" href="#">Contact</a></li>
  </ul> 
  <button>
    <img src="/images/menu.svg" class="p-2 w-20 md:hidden inline-flex"/>
  </button>
</nav>
