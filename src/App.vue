<script setup>
import Invitation from "./components/Invitation.vue";
import Countdown from "./components/Countdown.vue";

function scrollDown() {
    window.scroll(0, window.innerHeight);
}
</script>

<template>
    <div class="container">

        <div class="pt-5">
            <div class="text-uppercase container text-center text-invitation">Приглашаем на свадьбу</div>
        </div>

        <div class="names-box">
            <div class="names text-names">
                Баир <span class="d-lg-inline-block d-none">&</span> Алина
            </div>
        </div>

        <Countdown></Countdown>

        <div class="location">
            с. Усть-Кан, ул. Лесная, д. 51
        </div>

        <div class="time">
            <div class="left-hand hand">вс</div>
            <div class="day">30</div>
            <div class="right-hand hand">07</div>
        </div>

    </div>

    <Invitation ref="invitationElement"></Invitation>

    <div class="position-absolute w-100 bottom-0 justify-content-center d-flex">
        <button class="scroll mb-3 bg-none" style="background: none" @click="scrollDown()"></button>
    </div>
</template>

<style scoped>
.text-invitation {
    font-size: 1.7rem;
}
.names-box {
    font-size: 3rem;
    position: absolute;
    top: 25%;
    left: 0;
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
}

.names-box img {
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    background-color: #4158D0;
    background-image: linear-gradient(43deg, #4158D0 0%, #C850C0 46%, #FFCC70 100%);
    padding: 2px;
}

.names {
    font-family: 'French Kiss', serif;
    font-size: 5rem;
    color: #162a6d;
}

.location {
    position: absolute;
    bottom: 10%;
    left: 0;
    width: 100%;
    text-align: center;
}

.time {
    font-size: 1.7rem;
    position: absolute;
    bottom: 20%;
    left: 0;
    width: 100%;
    display: flex;
    align-items: center;
    text-transform: uppercase;
}

.time .day {
    width: 70px;
    line-height: 70px;
    font-size: 3rem;
    position: absolute;
    left: calc(50% - 35px);
    text-align: center;
    top: -38px;
}

.time .left-hand {
    position: absolute;
    right: calc(50% + 30px);
}

.time .right-hand {
    position: absolute;
    left: calc(50% + 30px);
}

.time .hand {
    border-top: 1px solid black;
    border-bottom: 1px solid black;
}

.day::after {
    font-size: 1.2rem;
    line-height: 1.2rem;
    content: '2023';
    position: absolute;
    left: calc(50% - 21px);
    bottom: -1rem;
}

.day::before {
    font-size: 1.2rem;
    line-height: 1.2rem;
    content: '10:00';
    position: absolute;
    left: calc(50% - 21px);
    top: -1rem;
}


</style>
