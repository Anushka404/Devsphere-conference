<script>
  export let name;
  export let title;
  export let image;
</script>


<div class="cursor-pointer">
  <a href="/speakers">
  <img class="w-80 h-80 mx-auto rounded-lg object-cover border-3 border-white
   hover:outline-4 hover:cursor-pointer hover:outline-violet-700" src={image} alt={name} />
  </a>
  <h3 class="text-lg font-semibold mt-3">{name}</h3>
  <p class="text-sm text-gray-500 dark:text-gray-400">{title}</p>
</div>