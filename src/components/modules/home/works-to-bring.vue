<template>
    <Transition name="slide">
        <div v-if="open" class="bg-white lg:px-10 lg:py-10 py-8 px-4  grid gap-11  lg:col-span-2">
            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid lg:gap-4 gap-8 lg:col-span-4 col-span-5 grid-cols-4">
                    <phone></phone>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">
                            Your Phone (or camera if you like)
                        </h1>
                    </div>
                </div>

            </div>

            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid lg:gap-4 gap-8 lg:col-span-4 col-span-5 grid-cols-4">
                    <shirts></shirts>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">
                            A few nice outfits (we have a changing room)
                        </h1>
                    </div>
                </div>


            </div>


            <div class="border border-[#E6E6E6] text-[#5C5C5C] grid grid-cols-5 items-center gap-8 p-4 rounded-lg ">

                <div class="lg:flex grid lg:gap-4 gap-8 lg:col-span-4 col-span-5 grid-cols-4">
                    <happy></happy>
                    <div class="col-span-3">
                        <h1 class="text-[16px] font-700">
                            Your happy self
                        </h1>
                    </div>
                </div>

            </div>
        </div>

    </Transition>
</template>

<script setup>
import phone from "../../icons/works-bring/phone.vue";
import shirts from "../../icons/works-bring/shirts.vue";
import happy from "../../icons/works-bring/happy.vue";

defineProps(['open'])
</script>