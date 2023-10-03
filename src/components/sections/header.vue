<template>
    <header :id="route.name == 'home' ? 'left-padded' : ''"
        class="lg:absolute  z-[1000] w-full lg:bg-transparent bg-white max-lg:!pl-0  py-[13px]  ">
        <nav class="bg-transparent border-gray-200 lg:px-[94px] px-[17px]">
            <div
                :class="'flex flex-wrap justify-between items-center mx-auto max-w-screen-xl ' + (route.name == 'booking' ? '!text-black' : 'text-white')">

                <div class="flex items-center lg:order-2 justify-between w-full">

                    <v-lazy-image src="/assets/images/logo.png" src-placeholder="https://placehold.it/350x250&text=1-retina"
                        class="bg-cover object-cover cursor-pointer w-[56px] lg:hidden" />

                    <!-- <a href="#"
                        class=" bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-3 lg:px-3 py-1 lg:py-1 mr-2  focus:outline-none border border-white rounded-md ">
                        Bookings
                    </a> -->
                    <button data-collapse-toggle="mobile-menu-2" type="button" id="hamburger"
                        class="inline-flex items-center p-2 ml-1 text-sm text-gray-500 rounded-lg lg:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 "
                        aria-controls="mobile-menu-2" aria-expanded="false">
                        <span class="sr-only">Open</span>
                        <svg class="w-6 h-6 open-icon" fill="#1C1B1F" viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd"
                                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                                clip-rule="evenodd"></path>
                        </svg>
                        <svg class="hidden w-6 h-6 close-icon" fill="#1C1B1F" viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd"
                                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                                clip-rule="evenodd"></path>
                        </svg>
                    </button>
                </div>
                <div :class="'lg:mt-0 mt-2 lg:rounded-none rounded-md hidden lg:justify-between items-center w-full lg:flex grid place-content-center text-center lg:w-full lg:order-1 lg:bg-transparent  z-[100]  ' + (route.name == 'booking' ? 'lg:!text-black !text-black' : 'lg:!text-white !text-black')"
                    id="mobile-menu-2">
                    <ul
                        class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0 lg:text-[14px] text-[32px] l">
                        <li>
                            <a href="/" class="block  pr-4 pl-3  lg:font-[400] font-[700] ">
                                Home
                            </a>
                        </li>
                        <li>
                            <a href="/about" class="block lg:hidden  pr-4 pl-3  lg:font-[400] font-[700] ">
                                About
                            </a>

                            <div class="lg:block hidden ">
                                <button id="mega-menu-dropdown-button" data-dropdown-toggle="mega-menu-dropdown"
                                    class="  pr-4 pl-3    ">
                                    <div class="flex items-center gap-2 text-inherit  ">
                                        <span class="font-[400]">About</span>
                                        <ArrowDown
                                            :fill="(route.name == 'booking' ? (mobile ? ('white') : ('black')) : 'white')"
                                            :width="12" :height="12"></ArrowDown>
                                    </div>
                                </button>
                                <div id="mega-menu-dropdown"
                                    class="absolute z-10 grid hidden  grid-cols-2 text-sm bg-white border border-gray-100 rounded-lg shadow-md  md:grid-cols-3 ">
                                    <div class="p-4  text-gray-900 md:pb-4 text-left ">
                                        <div class="space-y-4 grid" aria-labelledby="mega-menu-dropdown-button">

                                            <a href="/about" class="text-black   ">
                                                About Us
                                            </a>

                                            <a href="/about/#gallery" class="text-black   ">
                                                Gallery
                                            </a>

                                        </div>
                                    </div>
                                </div>

                            </div>
                        </li>
                        <li>
                            <a href="/#contact" class="block  pr-4 pl-3     lg:font-[400] font-[700] ">Contact</a>
                        </li>
                        <li>
                            <a href="/#faq" class="block  pr-4 pl-3     lg:font-[400] font-[700] ">Faq</a>
                        </li>

                    </ul>

                    <div class="lg:pt-4 lg:pb-4 pt-[58px] pb-[204px]  pl-3">
                        <a href="/booking" class=" "> <span
                                :class="' font-medium  lg:text-sm text-[16px] px-[11px] py-[8px]  mr-2  focus:outline-none border-[1px]  rounded-md   ' + (route.name == 'booking' ? '!border-black ' : 'lg:!border-white !border-black')">
                                Book Now
                            </span>
                        </a>
                    </div>
                </div>
            </div>
        </nav>
    </header>
</template>

<script setup>

import VLazyImage from "v-lazy-image";

import { onMounted } from 'vue';
import { Collapse } from 'flowbite';
import { useRoute } from 'vue-router';
import ArrowDown from '@/components/icons/arrow-down.vue';
import { mobile } from "../../mobile";


const route = useRoute();
// optional options with default values and callback functions
const options = {
    onCollapse: () => {
        $('.close-icon').addClass('hidden')
        $('.open-icon').removeClass('hidden')
    },
    onExpand: () => {
        $('.open-icon').addClass('hidden')
        $('.close-icon').removeClass('hidden')
    },
    onToggle: () => {
        // console.log('element has been toggled')
    }
};


onMounted(() => {

    const $targetEl = document.getElementById('mobile-menu-2');

    // optionally set a trigger element (eg. a button, hamburger icon)
    const $triggerEl = document.getElementById('hamburger');
    const collapse = new Collapse($targetEl, $triggerEl, options);
})
</script>

<style>
#left-padded {
    padding-left: 25%;
}
</style>