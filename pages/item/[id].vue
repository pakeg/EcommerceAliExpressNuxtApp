<template>
<div id="ItemPage" class="mt-4 max-w-[1200px] mx-auto px-2">
<div class="md:flex gap-4 justify-between mx-auto w-full">
<div class="md:w-[40%]">
<img v-if="currentImage" class="rounded-lg object-fit" :scr="currentImage"/>

<div v-if="images[0] !== ''" class="flex items-center justify-center mt-2">
<div v-for="image in images" :key="image">
<img @mouseover="currentImage = image"
@click="currentImage = image"
width="70"
class="rounded-md object-fit border-[3px] cursor-pointer"
:class="currentImage === image ? 'border-[#ff5353]' : ''"
:src="image"/>
</div>
</div>
</div>

<div class="md:w-[60%] bg-white p-3 rounded-lg">
<div v-if="true">
<p class="mb-2">Title</p>
<p class="font-light text-[12px] mb-2">Description Section</p>
</div>

<div class="flex items-center pt-1.5">
<span class="h-4 min-w-4 rounded-full p-0.5 bg-[#ffD000] mr-2">
<Icon name="material-symbols:star-rounded" class="-mt-[17px]" size="12"/>
</span>
<p class="text-[#ff5353]">Extra 5% off</p>
</div>

<div class="flex items-center justify-start my-2">
<Icon name="" color="#ff5353"/>
<span class="text-[13px] font-light ml-2">5 1234 Reviews 1,0000</span>
</div>
</div>

</div>
</div>
</template>

<script setup>
let currentImage = ref(null)
</script>