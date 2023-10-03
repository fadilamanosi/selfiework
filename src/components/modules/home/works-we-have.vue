<template>
    <Transition name="slide">
        <div v-if="open" class="bg-white  lg:px-10 lg:py-10 py-8 px-4  grid lg:grid-cols-3 grid-cols-1 gap-4  lg:col-span-2 ">
            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

               
                <div class="flex w-full gap-4 col-span-4 items-center">
                    <Ample></Ample>
                    <h1 class="text-[16px] font-700">Ample Parking</h1>
                </div>

            </div>

            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <ticket></ticket>
                    <h1 class=" w-full">10 Unique Booths</h1>
                </div>


            </div>


            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <wifi></wifi>
                    <h1 class="">Wifi</h1>
                </div>
            </div>

            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <wall></wall>
                    <h1 class="text-[16px] font-700">3 Themed Walls</h1>
                </div>

            </div>

            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <eyeglass></eyeglass>
                    <h1 class=" w-full">Great Props <br> (portable and set)</h1>
                </div>


            </div>


            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                   <room></room>
                    <h1 class="">Changing Room</h1>
                </div>
            </div>


            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <lights></lights>
                    <h1 class="text-[16px] font-700">Lights (ambient, ring, gear)</h1>
                </div>

            </div>

            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <accessory></accessory>
                    <h1 class=" w-full">Accessories (charging, set up, care and connectivity)</h1>
                </div>


            </div>


            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <music></music>
                    <h1 class="">Good Music and Speakers</h1>
                </div>
            </div>



            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <tripods></tripods>
                    <h1 class="text-[16px] font-700">Tripods</h1>
                </div>

            </div>

            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <remote></remote>
                    <h1 class=" w-full">Remote Shutters (phone compatible)</h1>
                </div>


            </div>


            <div class="border border-[#E6E6E6] h-fit text-[#5C5C5C]  items-center gap-8 p-4 rounded-lg ">

                <div class="flex w-full gap-4 col-span-4 items-center">
                    <mirrors></mirrors>
                    <h1 class="">Mirrors (lots of them)</h1>
                </div>
            </div>
        </div>

    </Transition>
</template>

<script setup>
import Ample from "../../icons/works-have/ample.vue";
import ticket from "../../icons/works-have/ticket.vue";
import wifi from "../../icons/works-have/wifi.vue";
import wall from "../../icons/works-have/wall.vue";
import room from "../../icons/works-have/room.vue";
import eyeglass from "../../icons/works-have/eyeglass.vue";

import lights from "../../icons/works-have/lights.vue";
import accessory from "../../icons/works-have/accessory.vue";
import music from "../../icons/works-have/music.vue";

import tripods from "../../icons/works-have/tripods.vue";
import remote from "../../icons/works-have/remote.vue";
import mirrors from "../../icons/works-have/mirrors.vue";



defineProps(['open'])
</script>