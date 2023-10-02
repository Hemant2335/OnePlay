<script >
	import { onMount } from "svelte"; 
    import PopMovies from "../components/PopMovies.svelte";
    import Navbar from "../components/Navbar.svelte";
    $: popular = [];
    async function load() {
      try {
        const apiKey = '11b7f92ac0548b80d7e51942d29f9d5b'; // Replace with your TMDb API key
        const url = `https://api.themoviedb.org/3/movie/popular?api_key=${apiKey}`;
  
        const res = await fetch(url);
        if (!res.ok) {
          throw new Error(`Failed to fetch data. Status: ${res.status}`);
        }
  
        const data = await res.json();
        popular = data?.results;
        if(res.ok){
            console.log(popular);
        }
      } catch (error) {
        console.error("An error occurred:", error);
      }
    }
    onMount(load);
</script>

<Navbar/>
<PopMovies movies = {popular}/>

<div class="grid grid-cols-4 mt-10">
{#each popular as pop}
<p>{pop?.original_title}</p>
{/each}
</div>