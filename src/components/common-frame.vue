<template>
    <div class="screen">
        <div class="navbar header">
            <div class="logo">
                <v-img contain width="42.96" height="48" src="/img/logo.svg"></v-img>
                <div class="logo-content">
                    <div class="text top-text-logo">ДОМ САЙТОВ</div>
                    <div class="text bottom-text-logo">УВЕЛИЧЕНИЕ ПРОДАЖ</div>
                </div>
            </div>
            <div class="text">Увеличиваем продажи в Вашем бизнесе!</div>
            <div class="text phone-text">+7 (4872) 79-29-10</div>
            <v-btn color="white" class="btn-call">
                <div class="phone-logo">
                    <v-img contain width="20" height="20" src="/img/phone.svg"></v-img>
                    <div class="text phone-text-logo ml-2">Заказать звонок</div>
                </div>
            </v-btn>
        </div>
        <v-divider />
        <div class="navbar items">
            <div v-for="(item, i) in items" :key="i">
                <v-btn flat small>
                    <div class="title-select" v-if="item === 'Увеличение продаж'">
                        <div class="text">{{item}}</div>
                        <v-img class="ml-1" contain width="10" height="5" src="/img/select.svg"></v-img>
                    </div>
                    <div v-else class="text">{{item}}</div>
                </v-btn>
            </div>
            <v-img contain width="24" height="24" src="/img/search.svg"></v-img>
        </div>
    </div>
</template>

<script>
import { ref } from "vue";
export default {
    setup() {
        const items = ref([
            "Увеличение продаж",
            "Создание сайтов",
            "Поддержка",
            "Битрикс 24",
            "О компании",
            "Отзывы",
            "Кейсы",
            "Контакты",
        ]);
        const selectItems = ref([
            "ПУНКТ 1",
            "SEO ПРОДВИЖЕНИЕ САЙТОВ В ЯНДЕКС",
            "ПРОВЕДЕНИЕ БИЗНЕСА В СОЦИАЛЬНЫХ СЕТЯХ",
            "ПУНКТ 4",
        ]);
        return {
            items,
            selectItems,
        };
    },
}
</script>

<style scoped lang="scss">
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .select {
        display: flex;
        flex-direction: row;
        align-items: center;
    }
    .header {
        height: 104px;
        .logo {
            display: flex;
            flex-direction: row;
            width: 185px;
            height: 48px;
            .logo-content {
                display: flex;
                flex-direction: column;
                justify-content: center;
                margin-left: 13.24px;
            }
        }
        .phone-logo {
            display: flex;
            flex-direction: row;
        }
    }
    .items {
        height: 80px;
        flex-wrap: wrap;
    }
    .title-select {
        display: flex;
        align-items: center;
    }
    .text {
        font-family: 'Montserrat';
        color: #212121;
        font-size: 14px;
        font-weight: 500;
        line-height: 17px;
        text-transform: uppercase;
    }
    .top-text-logo {
        font-weight: bold !important;
        font-size: 16px !important;
    }
    .bottom-text-logo {
        color: #333333 !important;
        font-size: 8.5px
    }
    .phone-text-logo {
        font-style: normal;
        color: #FF5900;
        font-size: 16px;
        text-align: center;
        letter-spacing: initial;
        text-transform: initial;
    }
    .phone-text {
        font-weight: 600;
        font-size: 16px;
        font-style: normal;
    }
    .btn-call {
        border-radius: 100px;
        border: 1px solid #FF5900;
        box-shadow: none !important;
        padding: 0;
        width: 222px;
        height: 52px;
    }
    .v-btn {
        padding-left: 0;
    }
}
.v-responsive {
    flex: none;
}
@media screen and (max-width: 1481px) {
    .items {
        justify-content: start;
    }
}
</style>