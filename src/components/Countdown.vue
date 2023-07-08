<script setup>
import VueCountDown from "@chenfengyuan/vue-countdown";
import {ref} from "vue";
const now = new Date();
const weddingTime = new Date('2023-07-30 10:00:00');
const time = weddingTime - now;
</script>

<template>
    <div class="countdown w-100">
        <div class="text-center">До свадьбы осталось:</div>
        <vue-count-down :time="time" v-slot="{days, hours, minutes, seconds}" class="d-flex justify-content-evenly time-container">
            <span data-content="дней">{{ days }}</span>
            <span data-content="часов">{{ hours }}</span>
            <span data-content="минут">{{ minutes }}</span>
            <span data-content="секунд">{{ seconds }}</span>
        </vue-count-down>
    </div>
</template>

<style scoped>
.countdown {
    position: absolute;
    bottom: 30%;
    left: 0;
    font-family: 'Tenor Sans', sans-serif;
}
.time-container span {
    font-size: 3rem;
    position: relative;
    width: 60px;
}
.time-container span::after {
    font-size: 1rem;
    content: attr(data-content);
    position: absolute;
    bottom: -5px;
    left: -5px;
}
</style>