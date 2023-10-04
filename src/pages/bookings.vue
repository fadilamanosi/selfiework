<template>
    <Header></Header>
    <section class="lg:pt-[130px] pt-[30px] lg:pb-[77px] pb-[30px] text-center">
        <h1 class="lg:text-[64px] text-[40px] font-[700] text-[#4D4D4D] text-center">Booking <br class="lg:hidden"> Tickets</h1>
    </section>

    <section class="lg:px-20 flex flex-col gap-[16px] px-4 pb-[80px]">

        <div class="relative  ">
            <div class="relative">
                <v-lazy-image src="/assets/images/booking.png" src-placeholder="/assets/images/blankSquare.png"
                    class="lg:max-h-[244px] lg:w-full cursor-pointer lg:block hidden " />

                <v-lazy-image src="/assets/images/bookingMobile1.png" src-placeholder="/assets/images/blankSquare.png"
                    class=" cursor-pointer block lg:hidden " />

                <div
                    class=" absolute top-0 text-white w-full h-full  grid grid-cols-5 place-content-center lg:px-20 gap-y-[27px] items-center px-[22px] z-[100]">
                    <div class=" lg:col-span-3 col-span-4">
                        <h1 class="text-[32px] font-bold pb-[20px]">Hourly Ticket</h1>
                        <p class="lg:text-[18px] text-[16px]">
                            60 Minutes of Selfie Goodness.
                            <br>
                            Capture moments alone, with your friends/family and create scroll-stopping content.
                        </p>
                    </div>

                    <div class="flex lg:justify-end lg:col-span-2 col-span-4">
                        <a onclick="Calendly.initPopupWidget({url: 'https://calendly.com/selfieworx'});return false;"
                            class=" font-medium  text-sm px-[11px] py-[8px] h-fit focus:outline-none border  rounded-md border-white w-fit">
                            Book Now
                        </a>
                    </div>
                </div>


            </div>
        </div>

        <div class="relative  ">
            <div class=" relative ">
                <v-lazy-image src="/assets/images/booking2.png" src-placeholder="/assets/images/blankSquare.png"
                    class=" lg:max-h-[244px] lg:w-full cursor-pointer lg:block hidden " />

                <v-lazy-image src="/assets/images/bookingMobile2.png" src-placeholder="/assets/images/blankSquare.png"
                    class=" cursor-pointer block lg:hidden  " />
                <div
                    class=" absolute top-0 text-white w-full h-full  grid grid-cols-5 place-content-center lg:px-20 gap-y-[27px] items-center px-[22px]  z-[100]">
                    <div class=" lg:col-span-3 col-span-4">
                        <h1 class="text-[32px] font-bold pb-[20px]">All Day Pass</h1>
                        <p class="lg:text-[18px] text-[16px]">
                            Explore our Booths and Installations all day.
                            <br class="lg:block hidden">
                            Come and go as you please without being limited to a timed session.
                        </p>
                    </div>

                    <div class="flex lg:justify-end lg:col-span-2 col-span-4">
                        <a onclick="Calendly.initPopupWidget({url: 'https://calendly.com/selfieworx'});return false;"
                            class=" font-medium  text-sm px-[11px] py-[8px] h-fit focus:outline-none border  rounded-md border-white w-fit">
                            Book Now
                        </a>
                    </div>
                </div>
            </div>
        </div>




        <div class="relative  ">
            <div class=" relative ">
                <v-lazy-image src="/assets/images/booking3.png" src-placeholder="/assets/images/blankSquare.png"
                    class="lg:max-h-[244px] lg:w-full cursor-pointer lg:block hidden " />

                <v-lazy-image src="/assets/images/bookingMobile2.png" src-placeholder="/assets/images/blankSquare.png"
                    class=" cursor-pointer block lg:hidden  " />
                <div
                    class=" absolute top-0 text-white w-full h-full  grid grid-cols-5 place-content-center lg:px-20 gap-y-[27px] items-center px-[22px] z-[100]">
                    <div class=" lg:col-span-3 col-span-4">
                        <h1 class="text-[32px] font-bold pb-[20px]">Private Events</h1>
                        <p class="lg:text-[18px] text-[16px]">
                            Enjoy Exclusivity & Freedom.
                            <br>
                            Rent our space for your private events and video shoots.
                        </p>
                    </div>

                    <div class="flex lg:justify-end lg:col-span-2 col-span-4">
                        <a onclick="Calendly.initPopupWidget({url: 'https://calendly.com/selfieworx'});return false;"
                            class=" font-medium  text-sm px-[11px] py-[8px] h-fit focus:outline-none border  rounded-md border-white w-fit">
                            Book Now
                        </a>
                    </div>
                </div>
            </div>
        </div>



    </section>
</template>

<script setup>
import VLazyImage from "v-lazy-image";
import Header from '@/components/sections/header.vue';




</script>

<style>
.gradient-cover-booking::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to right, #000000, #0000007D);
}


.gradient-cover-booking-mobile::after{
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to top, #000000, #00000000);
    
}
</style>