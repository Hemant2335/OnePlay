<script>
import "../app.css";
import logo from "../assets/logo1.png";
import profile from "../assets/profile.png";
</script>

<div class=" h-fit flex p-5 justify-between  items-center">

    <div>
    <img src={logo} alt="logo" class="h-[10vh]">
    </div>

    <nav class="flex gap-[5vh] items-center ">
        <ul class="flex  gap-[4vh] font-semibold">
            <li class="hover:text-red-400 cursor-pointer">Movies</li>
            <li class="hover:text-red-400 cursor-pointer">Series</li>
            <li class="hover:text-red-400 cursor-pointer">Animation</li>
            <li class="hover:text-red-400 cursor-pointer">Genres</li>
        </ul>
        <div class="flex gap-[2vh]">
            <input type="text" placeholder="Search" class="p-2 rounded-xl border-2 bg-[#222222] border-gray-300 w-[25vw] focus:outline-none focus:border-red-400">
        </div>
    </nav>
    

    <div class="">
        <img src={profile} alt="profile" class="w-[6vh] rounded-xl object-cover  ">
    </div>
</div>
