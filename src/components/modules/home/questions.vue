<template>
    <section id="faqs" class="min-h-screen bg-[#FCFCFC] lg:pt-[63px] pt-[54px] lg:px-[124px] pb-[66px] px-[17px] ">
        <div class="h-fit grid lg:gap-[47px] gap-[32px]">
            <h1 class="text-[#4D4D4D] lg:text-[64px] text-[40px] font-[700]  text-start leading-[64px]">
                Frequently <br class="lg:hidden"> asked questions</h1>
            <div class="grid lg:grid-cols-2 grid-cols-1 gap-x-6 gap-y-3 select-none">
                <div class=" grid gap-3">
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">What is your cancellation policy?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            All tickets are non-refundable; however you may RESCHEDULE ONCE for a later date/time at no
                            charge if you contact us prior to your appointment.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Do you take walk-ins?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Walk-ins are welcome, but not guaranteed as they are based on availability. We recommend booking
                            online or contacting us prior to your visit!
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">How do I purchase tickets?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            You can buy tickets online or you can buy tickets at the door, which are subject to
                            availability. Booking online is the only way to guarantee your appointment time.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">When should I arrive?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Please arrive 10-15 minutes prior to your scheduled appointment so we can check you in and get
                            you set up!
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Do I need to purchase a ticket even if I'm not taking pictures?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes. Everyone has to have a valid purchased ticket (taking photos or not) to gain admission
                            inside the Studio.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Does my child need a ticket? </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes. Infants (Under 3) are admitted for free with any paying adult (1 per adult) - CONFIRM/ IF
                            NOT EVERYONE SHOULD PAY
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Are you kid friendly?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Absolutely! All ages are welcome at Selfie Worx, but please keep in mind that we are not a
                            playground. All children under the age of 13 must be accompanied by an adult at all times. No
                            exceptions.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">If I only use 30 minutes instead of the full hour, can I come back &
                                use the other 30 minutes at a later time?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Unfortunately, your ticket can only be used once as we are not able to split your studio time
                            between two sessions.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Are food & beverages allowed inside?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Are food & beverages allowed inside?
                        </div>
                    </div>
                </div>

                <div v-show="!toggle" class="second-grid grid  gap-3 h-fit ">
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">
                                Do you have a changing room?
                            </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes. Selfie Worx has a changing room available for use, but do ask that all clients do not
                            occupy the changing room for more than ten minutes. The time spent in the restroom will count
                            towards your session. Try to be as prepared as possible so that you have more time to enjoy the
                            studio!
                        </div>
                    </div>

                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">
                                What should I bring with me?
                            </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Your phone or camera, your best self and any other accessories to create your best
                            content/moment. We recommend you leave bulky stuff (jackets, bags etc) in your car.
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">
                                Do You offer discounts for big groups?
                            </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes! We gladly offer discounted rates for groups of 8 or more people Monday-Thursday.
                        </div>
                    </div>

                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">
                                Can I bring my professional camera?
                            </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes you can. Unlike most places, we allow you to bring your DSLR at no extra charge! (but, we do
                            not allow your extra photography equipment)
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">
                                Can I shoot a music video at your venue?
                            </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Yes. It's nothing short of a brilliant idea! but this will require a Private Space Hire slot and
                            not during a Regular Ticket. This will give you full and exclusive use of the studio. For
                            reservations, please email us at bookings@selfieworx.com or call...
                        </div>
                    </div>

                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Can I bring my pet?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            We are pet lovers! But we do not allow dogs or any pets inside!
                        </div>
                    </div>
                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Do you alllow private events and team building?</p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Ofcourse! We are always happy to host private parties and team building events! For reservations
                            please email us at bookings@selfieworx.com or call...
                        </div>
                    </div>

                    <div class="bg-[#F6F6F6] px-6 py-4 text-[#4D4D4D] grid gap-8 h-fit cursor-pointer text-[16px]">
                        <div class=" flex justify-between items-center faqs ">
                            <p class="text-[#4D4D4D]">Do you have a resident photographer? </p>
                            <arrow-down></arrow-down>
                        </div>
                        <div class="hidden expanded">
                            Nahhhh. Every and anyone could be the photographer – work the selfies! We encourage guests to
                            return favours in photographong one another and that is always boundless fun.
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <div class="text-center pt-[46px] hover:underline lg:hidden block font-bold" @click="dropMore($event.target)">
            See all
        </div>

    </section>
</template>

<script setup>
import arrowDown from "@/components/icons/arrow-down.vue";
import { onBeforeMount, onMounted, ref } from "vue";
import { mobile } from "../../../mobile";


const toggle = ref(false);

function dropMore(e) {
    toggle.value = false
    $(e).addClass('hidden')
}


onMounted(() => {
    $('.faqs').on('click', function (e) {
        const p = $(e.currentTarget).siblings('.expanded');
        if (p.is(":visible")) {
            $(e.currentTarget).siblings('.expanded').addClass('hidden')
        } else {
            $(e.currentTarget).siblings('.expanded').removeClass('hidden')
        }
    })

})

onBeforeMount(() => {

    if (mobile) {
        toggle.value = true
    }

})

</script>