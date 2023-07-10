<script setup>
</script>

<template>
    <div class="invitation w-100">
        <div class="invitation-content w-100">
            <div class="text-center invitation__header">Приглашение</div>
            <div class="text-center container fz-3">
                Приглашаем Вас на нашу свадьбу!<br>
                Мы будем очень рады, если Вы проведете вместе с нами этот особенный день. <br>
            </div>
            <div class="text-center invitation__header">Программа</div>
            <div class="container fz-3">
                <div class="row">
                    <div class="col fz-5 text-end program-header__header">12:00</div>
                    <div class="col">
                        <div class="fz-3 program-header__header text-start">Белкенчек</div>
                        <div class="fz-2">с. Усть-Кан, ул. Космонавтов, д. 17</div>
                    </div>
                </div>
            </div>
            <div class="text-center invitation__header">Баир & Алина</div>
            <div class="container">
                <div class="d-flex flex-wrap justify-content-center gap-3 mb-3">
                    <div><img src="../assets/photos/6.jpg" alt="" class="rounded-3 shadow" width="300"></div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.program-header__header {
    font-weight: bold;
    color: #c2871d;
}

.fz-2 {
    font-size: 1rem;
}

.fz-5 {
    font-size: 2.5rem;
}

.fz-3 {
    font-size: 1.5rem;
}

.invitation {
    position: absolute;
    bottom: 0;
    left: 0;
}

.invitation__header {
    font-family: 'French Kiss', serif;
    font-size: 5rem;
    color: #664d24;
}

.invitation-content {
    position: absolute;
    top: 0;
    left: 0;
    min-height: 100vh;
    background-image: radial-gradient(circle 400px at 6.8% 8.3%, rgba(255, 244, 169, 1) 0%, rgba(255, 244, 234, 1) 100.2%);
}
</style>