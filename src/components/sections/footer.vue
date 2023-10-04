<template>
    <footer
        class=" lg:pt-[89px] pt-[44px] lg:px-[126px] pl-[17px] lg:pb-[51px] pb-[47px] grid lg:gap-y-[86px] gap-y-[80px] bg-[#F6F6F6] ">

        <div class="grid grid-cols-4  items-start lg:gap-0 gap-[46px]">
            <div class="lg:col-span-1 col-span-4">
                <!-- <img src="../assets/logo.png" alt="" class="w-[143px]"> -->
                <v-lazy-image src="/assets/images/logo.png" class="item cursor-pointer w-[100px]" />
            </div>
            <div class=" grid lg:place-items-center text-[#808080] gap-8 lg:col-span-2 col-span-4">
                <div class="flex lg:flex-row flex-col lg:gap-11 gap-[18px] text-lg text-[#4C4C4C] select-none w-max">
                    <a href="/#contact">Contact us</a>
                    <a href="/about">About Studio</a>
                    <a href="/#how">How it works</a>
                    <a href="/#faqs">FAQs</a>
                </div>
            </div>

            <div class="flex lg:justify-end">
                <div class="flex gap-[40px] flex-end">
                    <facebook :fill="'#4D4D4D'"></facebook>
                    <twitter :fill="'#4D4D4D'"></twitter>
                    <instagram :fill="'#4D4D4D'"></instagram>
                </div>
            </div>

            <div class=" grid lg:text-[16px] text-[14px] col-span-4 lg:place-content-center lg:text-center text-[#7F7F7F]">
                <div class="flex lg:items-center lg:gap-11 gap-4">
                    <div class="flex items-center gap-2 ">
                        <envelope></envelope>
                        <a href="mailto:hello@selfieworkx.com" class="text-sm">hello@selfieworkx.com</a>
                    </div>
                    <div class="flex items-center gap-2 ">
                        <phone></phone>
                        <a href="tel:+44 7342 741922" class="text-sm">+44 7342 741922</a>
                    </div>
                </div>
                <div class="col-span-2">
                    <span class=" text-sm">Unit UGJ, 9 Bradstone Road, Manchester M88WA</span>
                </div>
            </div>
        </div>

        <div class="text-xs text-[#656565] font-400">
            Copyright © 2023. Selfie Worx. All rights reserved.
        </div>
    </footer>
</template>
<script setup>

import VLazyImage from "v-lazy-image";


import facebook from "@/components/icons/facebook.vue"
import twitter from "@/components/icons/twitter.vue"
import instagram from "@/components/icons/instagram.vue"


import phone from "@/components/icons/phone.vue"
import envelope from "@/components/icons/envelope.vue"




</script>

