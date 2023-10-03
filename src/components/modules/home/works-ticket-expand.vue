<template>
    <Transition name="slide">
        <div v-if="open" class="bg-white lg:p-10 p-4 grid gap-11 slideIn lg:col-span-2">
            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid gap-4 lg:col-span-4 col-span-5 grid-cols-4">
                    <div class=" ">
                        <ticketList></ticketList>
                    </div>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">Hourly Ticket</h1>
                        <p class="text-[12px]">
                            60 minutes of Selfie Goodness.
                            Capture moments alone, with your friends/family or create scroll-stopping content.
                        </p>
                    </div>
                </div>

                <div class="w-full flex lg:justify-end lg:col-span-1 col-span-4 lg:col-start-auto col-start-2 lg:pl-0 pl-3">
                    <a href="/booking"
                        class=" text-[#5C5C5C] bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-4 py-2 focus:outline-none border border-[#5C5C5C] rounded-md w-max h-fit ">
                        Book Now
                    </a>
                </div>
            </div>

            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid gap-4 lg:col-span-4 col-span-5 grid-cols-4">
                    <div class=" ">
                        <ticketList></ticketList>
                    </div>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">Hourly Ticket</h1>
                        <p class="text-[12px]">
                            60 minutes of Selfie Goodness.
                            Capture moments alone, with your friends/family or create scroll-stopping content.
                        </p>
                    </div>
                </div>

                <div class="w-full flex lg:justify-end lg:col-span-1 col-span-4 lg:col-start-auto col-start-2 lg:pl-0 pl-3">
                    <a href="/booking"
                        class=" text-[#5C5C5C] bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-4 py-2 focus:outline-none border border-[#5C5C5C] rounded-md w-max h-fit ">
                        Book Now
                    </a>
                </div>
            </div>
            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid gap-4 lg:col-span-4 col-span-5 grid-cols-4">
                    <div class=" ">
                        <ticketList></ticketList>
                    </div>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">Hourly Ticket</h1>
                        <p class="text-[12px]">
                            60 minutes of Selfie Goodness.
                            Capture moments alone, with your friends/family or create scroll-stopping content.
                        </p>
                    </div>
                </div>

                <div class="w-full flex lg:justify-end lg:col-span-1 col-span-4 lg:col-start-auto col-start-2 lg:pl-0 pl-3">
                    <a href="/booking"
                        class=" text-[#5C5C5C] bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 font-medium  text-sm px-4 py-2 focus:outline-none border border-[#5C5C5C] rounded-md w-max h-fit ">
                        Book Now
                    </a>
                </div>
            </div>
        </div>
    </Transition>
</template>

<script setup>
import ticketList from "../../icons/ticket-list.vue";


defineProps(['open'])
</script>





<!-- 
<style>
.slideIn {
    animation-duration: 3s;
    animation-name: slidein;
}

@keyframes slidein {
    from {
        /* margin-left: 100%; */
        width: 20%;
    }

    to {
        /* margin-left: 0%; */
        width: 80%;
    }
}
</style> -->