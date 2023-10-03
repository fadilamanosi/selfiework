<template>
    <Header></Header>
    <section class="flex h-screen">
        <div class=" lg:w-[25%]  lg:grid hidden place-content-center ">
            <img src="../assets/logo.png" alt="" class="w-[143px]">
        </div>

        <div class=" bg-no-repeat bg-cover bg-center lg:w-[80%] w-full relative ">
            <Splide :options="options" aria-label="My Favorite Images">
                <SplideSlide class="relative">
                    <v-lazy-image src="/assets/images/home/home1.png" src-placeholder="/assets/images/home/home1poor.png"
                        class="item home-imgs h-full bg-cover object-cover cursor-pointer" />

                    <div
                        class="lg:text-[116px] text-[64px] absolute lg:bottom-28 bottom-0 text-[#FFFFFF] leading-[1em]  w-full lg:h-auto h-full lg:block flex  flex-col justify-center  text-center select-none font-[700]">
                        Immersive <br> spaces
                    </div>
                </SplideSlide>
                <SplideSlide>
                    <v-lazy-image src="/assets/images/home/home2.png" src-placeholder="/assets/images/home/home2poor.png"
                        class="item home-imgs h-full bg-cover object-cover cursor-pointer" />

                    <div
                        class="lg:text-[116px] text-[64px] absolute lg:bottom-28 bottom-0 text-[#FFFFFF] leading-[1em]  w-full lg:h-auto h-full lg:block flex  flex-col justify-center  text-center select-none font-[700]">
                        Charming <br> Selfies
                    </div>
                </SplideSlide>

                <SplideSlide>
                    <v-lazy-image src="/assets/images/home/home3.png" src-placeholder="/assets/images/home/home3poor.png"
                        class="item home-imgs h-full bg-cover object-cover cursor-pointer" />

                    <div
                        class="lg:text-[116px] text-[64px] absolute lg:bottom-28 bottom-0 text-[#FFFFFF] leading-[1em]  w-full lg:h-auto h-full lg:block flex  flex-col justify-center  text-center select-none font-[700]">
                        Unforgettable <br> Moments
                    </div>
                </SplideSlide>
            </Splide>
        </div>

    </section>

    <section class="  relative">

        <Splide :options="sectionTwoOption" aria-label="My Favorite Images">
            <SplideSlide>
                <v-lazy-image src="/assets/images/studio/studio1.png" src-placeholder="/assets/images/blankSquare.png"
                    class="item home-imgs bg-cover object-cover cursor-pointer" />
            </SplideSlide>
            <SplideSlide>
                <v-lazy-image src="/assets/images/studio/studio2.png" src-placeholder="/assets/images/blankSquare.png"
                    class="item home-imgs bg-cover object-cover cursor-pointer" />
            </SplideSlide>
            <SplideSlide>
                <v-lazy-image src="/assets/images/studio/studioAll.png" src-placeholder="/assets/images/blankSquare.png"
                    class="item home-imgs bg-cover object-cover cursor-pointer" />
            </SplideSlide>
        </Splide>

        <div class="absolute top-0 text-center grid place-content-center w-full h-full text-white">
            <div class="flex flex-col ">
                <div class="flex flex-col ">
                    <h1 class="text-[64px] font-[700] leading-10">Our Studio</h1>
                    <p class="font-400 text-[16px] pt-[16px]">Selfie Worx is Manchester's Creative Post-ready Content Boutique.</p>
                </div>
                <div class="flex justify-center pt-[36px]">
                    <a href="/booking"
                        class=" text-white  font-medium  text-[16px]  px-[11px] py-[8px] focus:outline-none border border-white rounded-md w-fit ">
                        Book now
                    </a>
                </div>
            </div>
        </div>

    </section>

    <Works></Works>

    <Questions></Questions>


    <Contact></Contact>
</template>

<!-- bg-[url(../assets/images/home1.png)] -->
<script setup>
import VLazyImage from "v-lazy-image";
import { onBeforeMount, onMounted, ref } from "vue";
import { Splide, SplideSlide } from '@splidejs/vue-splide';

import arrowOpen from "@/components/icons/arrow-open.vue";
import arrowDown from "@/components/icons/arrow-down.vue";

import Header from '@/components/sections/header.vue';

import { mobile } from "../mobile";

import Works from "@/components/modules/home/works.vue";
import Questions from "@/components/modules/home/questions.vue";
import Contact from "@/components/sections/contact.vue";


const options = ref({
    rewind: true,
    gap: '1rem',
    direction: 'ttb',
    height: '100vh',
    arrows: false,
    autoplay: true,
    speed: 500,
    interval: 5000,
    pauseOHover: true,
    classes: {
        pagination: 'splide__pagination paginate-div', // container
        page: 'splide__pagination__page paginate-icon', // each button
    }
})




const sectionTwoOption = {
    rewind: true,
    gap: '1rem',
    height: '100vh',
    arrows: false,
    autoplay: true,
    speed: 500,
    interval: 5000,
    type: 'fade',
    pagination: false,

}


window.addEventListener('resize', function () {
    if (mobile) {
        options.value.direction = 'rtl'
    } else {
        options.value.direction = 'ttb'
    }
})

onBeforeMount(() => {

    if (mobile) {
        options.value.direction = 'rtl'
        // options.value.classes.pagination ='splide__pagination paginate-div mobile-paginate'
    }



})
</script>



<style scoped>
.home-imgs {
    width: 100%;
    height: 100vh;
}
</style>