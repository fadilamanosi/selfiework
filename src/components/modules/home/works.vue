<template>
    <section id="how" class="h-fit bg-[#CD019F] relative lg:px-[124px] px-[17px] lg:pb-[117px] pb-[36px]">
        <div class="grid  lg:pt-[67px] pt-[53px]  ">
            <div class="grid place-content-center w-full text-white">
                <div class="text-center lg:w-[661px] lg:px-0 px-[18px] ">
                    <h1 class="lg:text-[64px] font-[700] leading-[64px] text-[40px]">How it Works</h1>
                    <p class="text-[14px] font-400 lg:pt-[24px] pt-[16px]">Selfie Worx is the perfect place for anyone
                        looking to upgrade their
                        selfie game; generate creative
                        content
                        for
                        social media; make memories with their tribe or just looking for a cool place to visit.</p>
                </div>
            </div>

            <div class="works-box-parent grid lg:grid-cols-3 lg:gap-2 gap-6 lg:flex-nowrap flex-wrap lg:pt-[66px] pt-[48px] h-fit">
                <div class="works-box  relative  lg:h-[558px] md:h-full min-h-[558px]   ">
                    <div class="gradient-cover-works relative h-full">
                        <v-lazy-image src="/assets/images/how/how1.png" src-placeholder="/assets/images/blankRec.png"
                            class="item cursor-pointer h-full w-full relative" />

                        <div class="absolute bottom-0 w-full  text-white z-50 grid gap-[72px] p-8">
                            <div class="grid gap-[12px] pr-8">
                                <span class="text-[18px]">Booking Tickets</span>
                                <span class="text-[14px]">
                                    Start by booking your session at our studio.
                                    You can reserve your slot online or give us a call.
                                </span>
                            </div>


                            <div @click="slide($event.target, 'ticket')"
                                class="flex items-center gap-2 text-[14px] cursor-pointer hover:underline">

                                <div v-if="expand.view == 'ticket'" class="flex items-center gap-2">
                                    <span>See less</span>
                                    <arrow-close></arrow-close>
                                </div>

                                <div v-else class="flex items-center gap-2">
                                    <span>See more</span>
                                    <arrow-open></arrow-open>
                                </div>


                            </div>
                        </div>
                    </div>
                </div>

                <div class="relative  works-box lg:h-[558px] md:h-full min-h-[558px]   ">
                    <div class="gradient-cover-works relative   h-full">
                        <v-lazy-image src="/assets/images/how/how2.png  " src-placeholder="/assets/images/blankRec.png"
                            class="item cursor-pointer   relative  h-full w-full" />

                        <div class="absolute bottom-0 w-full  text-white z-50 grid gap-8 p-8">
                            <div class="grid gap-3 pr-8">
                                <span class="text-[18px]">What to bring</span>
                                <span class="text-[14px]">
                                    On the day of your session, arrive at our studio early. Our friendly staff will
                                    welcome
                                    you and get you set up.
                                </span>
                            </div>


                            <div @click="slide($event.target, 'bring')"
                                class=" gap-2 text-[14px] cursor-pointer hover:underline">

                                <div v-if="expand.view == 'bring'" class="flex items-center gap-2">
                                    <span>See less</span>
                                    <arrow-close></arrow-close>
                                </div>

                                <div v-else class="flex items-center gap-2">
                                    <span>See more</span>
                                    <arrow-open></arrow-open>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="relative  works-box  lg:h-[558px] md:h-full min-h-[558px] ">
                    <div class="gradient-cover-works relative  h-full ">
                        <v-lazy-image src="/assets/images/how/how3.png" src-placeholder="/assets/images/blankRec.png"
                            class="item cursor-pointer  relative  h-full w-full" />

                        <div class="absolute bottom-0 w-full  text-white z-50 grid gap-8 p-8">
                            <div class="grid gap-3 pr-8">
                                <span class="text-[18px]">What we have</span>
                                <span class="text-[14px]">
                                    Our studio is set up to make your experience memorable, hitch-free and very
                                    productive.
                                </span>
                            </div>


                            <div @click="slide($event.target, 'have')"
                                class="flex items-center gap-2 text-[14px] cursor-pointer hover:underline">
                                <div v-if="expand.view == 'have'" class="flex items-center gap-2">
                                    <span>See less</span>
                                    <arrow-close></arrow-close>
                                </div>

                                <div v-else class="flex items-center gap-2">
                                    <span>See more</span>
                                    <arrow-open></arrow-open>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>


                <works-ticket-expand :open="expand.view == 'ticket' ? true : false"></works-ticket-expand>
                <works-to-bring :open="expand.view == 'bring' ? true : false"></works-to-bring>
                <works-we-have :open="expand.view == 'have' ? true : false"></works-we-have>

            </div>
        </div>
    </section>
</template>

<script setup>
import VLazyImage from "v-lazy-image";

import arrowOpen from "@/components/icons/arrow-open.vue";
import arrowClose from "@/components/icons/arrow-close.vue";


import worksWeHave from "@/components/modules/home/works-we-have.vue";
import worksToBring from "@/components/modules/home/works-to-bring.vue";
import worksTicketExpand from "@/components/modules/home/works-ticket-expand.vue";
import { ref } from "vue";

const expand = ref({
    toggle: false,
    view: ''
})

function slide(e, p) {

    if (expand.value.view) {
        expand.value.toggle = false

        //Slideout
        setTimeout(() => {
            $('.works-box').removeClass('hidden')
        }, 10)
        expand.value.view = ''

        // Add gap
        $('.works-box-parent').removeClass('!gap-0')
    } else {
        expand.value.toggle = true

        // slide in
        $('.works-box').addClass('hidden')
        $(e).parents('.works-box').removeClass('hidden')
        expand.value.view = p

        // Remove gap
        $('.works-box-parent').addClass('!gap-0')

    }


}
</script>

<style>
.gradient-cover-works::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0.108), rgba(0, 0, 0, 0.7));
}
</style>

