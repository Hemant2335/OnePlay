<script>
import "../app.css";
import logo from "../assets/logo1.png";
import profile from "../assets/profile.png";
</script>

<div class=" h-[15vh] flex p-5 justify-between  items-center">

    <div class="flex">
    <h1 class="font-bold text-3xl text-red-400">ONE</h1>
    <h1 class="font-bold text-3xl ">PLAY</h1>
    </div>



    <div class="flex items-center gap-[5vh]">
        
        <div class="flex gap-[2vh]">
            <input type="text" placeholder="Search" class="p-2 rounded-lg border-2 bg-[#222222] border-gray-300 w-[25vw] focus:outline-none focus:border-red-400">
        </div>
        <img src={profile} alt="profile" class="w-[6vh] rounded-xl object-cover  ">
    </div>
</div>
