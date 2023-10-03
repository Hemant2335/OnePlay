<script>
    import { onMount } from "svelte"; 
    import {useFetch} from "../hooks/useFetch.js";
    $: popular = [];
    async function load() {
      try {
        const endpoint = "popular";
        popular = await useFetch(endpoint);  
        console.log(popular);    
      } catch (error) {
        console.log(error)
      }
    }
      
    onMount(load);
</script>

<h1 class="text-2xl font-semibold p-4">Popular</h1>
<div class="p-[5vh]  flex flex-col">
    
    <div class="grid grid-cols-4">
        {#each popular as movie}
        <div class="p-2">
            <img src={"https://image.tmdb.org/t/p/w500/" + movie.poster_path} alt="poster" class="w-[15vw] rounded-xl object-cover">
            <p class="text-sm font-semibold">{movie.original_title}</p>
        </div>
        {/each}
    </div>
</div>