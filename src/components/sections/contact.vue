<template>
    <section id="contact" class="lg:min-h-screen bg-cover  relative">
        <div class="gradient-cover-contact">
            <v-lazy-image src="/assets/images/contact.png" src-placeholder="/assets/images/blankSquare.png"
                class="item cursor-pointer lg:h-screen w-full h-[562px]  object-cover relative gradient-cover-contact hidden md:block" />

            <v-lazy-image src="/assets/images/contactMobile.png"
                src-placeholder="/assets/images/blankSquare.png" class="md:hidden block h-[562px] w-full"></v-lazy-image>

            <div
                class="grid  text-white absolute top-0 w-full lg:h-fit  z-50 lg:pt-[107px] pt-[53px] lg:pl-[130px] pl-[17px] ">
                <h1 class="text-white lg:text-[64px] text-[40px] font-[700] leading-[64px] pb-[42px]">
                    Contact us
                </h1>

                <div class="grid pb-[24px] gap-[6px]">
                    <p class="text-[#999] lg:text-base text-xs">Open Hours</p>
                    <p class="lg:text-xl text-sm">
                        Monday - Friday: <span class="font-bold  ">9am - 7pm</span>
                    </p>
                    <p class="lg:text-xl text-sm">
                        Saturday - Sunday: <span class="font-bold">10am - 6pm</span>
                    </p>
                </div>

                <div class="grid h-fit gap-[6px]">
                    <span class="text-[#999999] pb-[14px] lg:text-base text-xs">Social Media</span>

                    <div class="flex gap-[14px] items-center pb-[44px] ">
                        <div class="flex gap-2">
                            <facebook :fill="'white'"></facebook>
                            <twitter :fill="'white'"></twitter>
                            <instagram :fill="'white'"></instagram>
                        </div>
                        <span class="lg:text-xl text-sm">Selfieworx</span>
                    </div>
                    
                </div>

                <a href="https://maps.app.goo.gl/atEZxorx88mgqceL8" target="_blank"
                    class="h-fit  text-white bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-[11px] py-[8px] focus:outline-none border border-white rounded-md w-fit ">
                    See Map
                </a>
            </div>
        </div>
    </section>
</template>
<script setup>
import VLazyImage from "v-lazy-image";

import facebook from "@/components/icons/facebook.vue"
import twitter from "@/components/icons/twitter.vue"
import instagram from "@/components/icons/instagram.vue"
</script>

<style>
.gradient-cover-contact::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to right, #000000, #00000000);


}
</style>