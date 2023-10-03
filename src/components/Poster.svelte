<script>
    import { onMount } from "svelte"; 
    import {useFetch} from "../hooks/useFetch.js";
    $: poster = [];
    async function load() {
      try {
        const endpoint = "upcoming";
        poster = await useFetch(endpoint);  
        console.log(poster);    
      } catch (error) {
        console.log(error)
      }
    }
    onMount(load);
</script>

    <div class="snap-x scroll-px-4 h-[50vh] snap-mandatory scroll-smooth flex gap-4 overflow-x-auto px-4 py-10">
        {#each poster as movie} 
            <img src={"https://image.tmdb.org/t/p/w500/" + movie.poster_path} alt="poster" class="w-full h-full rounded-md object-cover">
        {/each}
    </div>
