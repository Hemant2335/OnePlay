<script>
    export let movies;
</script>


<div class="p-4">
    <h1 class="text-xl font-semibold">Popular</h1>
    <div class="grid grid-cols-4">
        {#each movies as movie}
        <div class="p-2">
            <img src={"https://image.tmdb.org/t/p/w500/" + movie.poster_path} alt="poster" class="w-[15vw] rounded-xl object-cover">
            <p class="text-sm font-semibold">{movie.original_title}</p>
        </div>
        {/each}
    </div>
</div>