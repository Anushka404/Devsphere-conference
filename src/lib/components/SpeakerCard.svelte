<script>
    export let name;
    export let title;
    export let image;
  </script>
  
  <div class="bg-gray-800 text-white p-4 rounded-lg shadow-lg text-center">
    <img class="w-24 h-24 mx-auto rounded-full object-cover border-4 border-violet-500" src={image} alt={name} />
    <h3 class="text-lg font-semibold mt-3">{name}</h3>
    <p class="text-sm text-gray-400">{title}</p>
  </div>
  