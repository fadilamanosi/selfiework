<template>
    <svg :width=" width ?? 8" :height="height ?? 17" viewBox="0 0 8 17" :fill="fill ?? 'none'" xmlns="http://www.w3.org/2000/svg">
        <path
            d="M6.53267 3.60022H7.9917V1.05907C7.73998 1.02445 6.87429 0.946533 5.86609 0.946533C3.76245 0.946533 2.3214 2.26972 2.3214 4.70165V6.93981H0V9.78062H2.3214V16.9286H5.16754V9.78129H7.39504L7.74864 6.94048H5.16687V4.98334C5.16754 4.16226 5.38862 3.60022 6.53267 3.60022Z"
            :fill="fill ?? 'white'" />
    </svg>
</template>

<script setup>
defineProps(['fill', 'width', 'height'])
</script>