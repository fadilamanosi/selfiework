<template>
    <Header></Header>
    <section class=" relative ">
        <div class=" gradient-cover-about  ">
            <v-lazy-image src="/assets/images/about1.png" src-placeholder="/assets/images/blankSquare.png"
                class=" h-screen  cursor-pointer w-full lg:block hidden" />

                <v-lazy-image src="/assets/images/aboutMobile.png" src-placeholder="/assets/images/blankSquare.png"
                class=" h-[767px] cursor-pointer w-full  block lg:hidden" />

                
            <div class="w-full h-fit absolute text-center text-white z-50 top-0 flex justify-center lg:px-0 px-[33px]  pt-[71px] lg:pt-[121px] ">
                <div class="lg:w-[662px] grid lg:gap-11 gap-8">
                    <h1 class="lg:text-[116px] text-[40px] font-[700] ">About Us</h1>

                    <div class="grid gap-8 ">
                        <p class="lg:text-[18px] text-[16px] font-[500]">Selfie Worx is Manchester's Creative One-stop Post-ready Content Boutique.
                        </p>

                        <p class="text-[14px]  lg:px-11 px-[12px]">
                            Equipped with 10 beautifully designed booths and 3 feature-theme walls, our studio provides a
                            unique
                            and
                            immersive experience; offering creative selfie opportunities and picturesque themes and props
                            for
                            creating memorable moments.
                        </p>
                        <p class="text-[14px] lg:px-11 px-[12px]">
                            Create surreal images, videos and content that worx as you explore our captivating spaces for
                            your
                            personal or group use and business needs – there's a perfect spot for you!
                        </p>
                    </div>

                    <b class="lg:text-[14px]  lg:px-24 px-[12px]"> 
                        Book your next shoot with us with an hourly ticket, all day pass or private event/party hire – you
                        are
                        more than welcome!
                    </b>

                    <div class="pb-[44px]">
                        <a href="#"
                            class="text-white bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-3 lg:px-3 py-2   focus:outline-none border border-white rounded-md ">
                            Book Now
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery" class="min-h-screen ">
        <div class="relative lg:px-28 px-[17px] pb-[32px]">


            <div class="w-full h-full  text-center text-[#4D4D4D] z-50 top-0 grid place-content-center pt-[71px] pb-[75px] ">
                <div class="lg:w-[662px] grid h-fit">
                    <h1 class="lg:text-[116px] text-[40px] pb-[32px] font-[700]">Our Gallery</h1>

                    <div class="grid gap-[20px] pb-[52px]">
                        <p class="text-[18px]">
                            See our enchanting spaces, installations and themes
                        </p>

                        <p class="font-400">
                            Our props, equipment and staff are always available to make your personal or professional shoots
                            fun, productive and everything in-between. Have a look.
                        </p>
                    </div>

                    <div class="flex justify-center items-center gap-2"> 
                        <span>Let's Connect</span>
                        <facebook :fill="'black'"></facebook>
                        <instagram :fill="'black'"></instagram>
                    </div>
                </div>
            </div>


            <div class="grid lg:grid-cols-3 grid-cols-1  place-content-center  lg:gap-4 gap-y-[16px] lg:gradient-cover-gallery relative">
                <v-lazy-image src="/assets/images/about2.png" src-placeholder="/assets/images/blankSquare.png"
                    class="  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about3.png" src-placeholder="/assets/images/blankSquare.png"
                    class="  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about4.png" src-placeholder="/assets/images/blankSquare.png"
                    class="  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about5.png" src-placeholder="/assets/images/blankSquare.png"
                    class=" h-full  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about6.png" src-placeholder="/assets/images/blankSquare.png"
                    class="  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about7.png" src-placeholder="/assets/images/blankSquare.png"
                    class="  object-cover cursor-pointer max-h-[523px] w-full " />
                <v-lazy-image src="/assets/images/about8.png" src-placeholder="/assets/images/blankSquare.png"
                    class="h-full   object-cover cursor-pointer max-h-[523px] w-full " /> 
            </div>
        </div>
    </section>

    <Contact></Contact>
</template>

<script setup>
import Header from '@/components/sections/header.vue';

import VLazyImage from "v-lazy-image";
import Contact from "@/components/sections/contact.vue";

import facebook from "@/components/icons/facebook.vue";
import instagram from "@/components/icons/instagram.vue";
</script>


<style>
.gradient-cover-about::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to left, rgba(255, 255, 255, 0.108), rgba(0, 0, 0, 0.883));
}


.gradient-cover-gallery::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(0, 0, 0, 0.639));
}
</style>