<template>
    <div class="header bg-white flex justify-between items-center p-4 sticky top-0 z-50">
        <div class="name flex items-center text-2xl font-bold">
            <i class="fas fa-a bg-black text-white rounded-full px-3 py-2"></i>
            <span class="ml-2 slide-in">Asude Ruken Kalğı</span>
        </div>
        <!-- linkler büyük ekran -->
        <div class="hidden md:flex gap-4 items-center">
            <a href="#about" class="px-3 py-2 rounded-[20px] hover:bg-gray-200">About</a>
            <a href="#projects" class="px-3 py-2 rounded-[20px] hover:bg-gray-200">My Projects</a>
            <a href="#accounts" class="px-3 py-2 rounded-[20px] hover:bg-gray-200">Social Media Accounts</a>
            <div class="mode-icons cursor-pointer text-lg">
                <i class="fa-regular fa-sun" @click="$emit('toggleTheme')" v-if="!isDark"></i>
                <i class="fa-solid fa-moon" @click="$emit('toggleTheme')" v-if="isDark"></i>
            </div>
        </div>

        <!-- hamburger küçük ekran -->
        <div class="md:hidden">
            <button @click="open = !open" class="text-2xl focus:outline-none  cursor-pointer">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </div>

    <!-- mobil menü -->
    <div v-if="open" class="md:hidden bg-white flex flex-col gap-2 p-4">
        <a href="#about" class="px-3 py-2 rounded hover:bg-gray-200">About</a>
        <a href="#projects" class="px-3 py-2 rounded hover:bg-gray-200">My Projects</a>
        <a href="#accounts" class="px-3 py-2 rounded hover:bg-gray-200">Social Media Accounts</a>
        <div class="mode-icons cursor-pointer text-lg pl-3">
            <i class="fa-regular fa-sun" @click="$emit('toggleTheme')" v-if="!isDark"></i>
            <i class="fa-solid fa-moon" @click="$emit('toggleTheme')" v-if="isDark"></i>
        </div>
    </div>
    <div class="line border-b-2 border-black"></div>
</template>

<script>
export default {
  props: ['isDark'],
  data() {
    return {
      open: false
    }
  }
}
</script>


<style>
html{
    background-color: rgb(219, 217, 217);
    scroll-behavior: smooth;
}

.slide-in{
    display: inline-block;
    animation:slideRight 2s ease-in-out forwards;
}
@keyframes slideRight{
    from{
        opacity: 0;
        transform: translateX(-45px);
    }
    to{
        opacity: 1;
        transform: translateX(0);
    }
}

</style>