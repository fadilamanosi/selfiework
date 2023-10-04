
<template>
    <router-view></router-view>
    <Footer></Footer>
</template>

<script setup>
import Footer from '@/components/sections/footer.vue';
import { onMounted } from 'vue';


onMounted(() => {


})
</script>



<style>
.slide-enter-from {
    opacity: 0;
    transform: translateX(-60px);
}

.slide-enter-to {
    opacity: 1;
    transform: translateX(0px);
}

.slide-enter-active {
    transition: all 0.5s ease;
}

.home-imgs {
    width: 100%;
    height: 100vh;
}

.gradient-cover-works::after {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(255, 255, 255, 0.108), rgba(0, 0, 0, 0.7));
}



/* .slide-leave-from {
    opacity: 1;
    transform: translateX(60px);
}


.slide-leave-to {
    opacity: 0;
    transform: translateX(-60px);
}

.slide-leave-active {
    transition: all 0.5s ease;
} */


/* .slidein {
    animation-duration: 3s;
    animation-name: slidein;
}

@keyframes slidein {
    from {
        opacity: 0;
        transform: translateX(0px);
    }

    to {
        opacity: 1;
    transform: translateX(60px);
    }
} */
</style>

