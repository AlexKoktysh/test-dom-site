<template>
    <div class="digital">
        <div class="text"><span class="color-text">Антикризисные </span>DIGITAL-пакеты</div>
        <div class="card-block">
            <div v-for="(card, i) in cardItems" :key="i">
                <DigitalCard :cardItem="cardItems[i]" />
            </div>
        </div>
    </div>
</template>

<script>
import DigitalCard from './digital-card.vue'
import { ref } from "vue";
export default {
    components: {
        DigitalCard,
    },
    setup() {
        const cardItems = ref([
            {
                src: "/img/stable-card.png",
                gradient: "linear-gradient(180deg, rgba(51, 51, 51, 0) 0%, #333333 86.98%)",
                header: "Стабильная лидогенерация в кризис",
                text: [
                    "SEO-продвижение + Контекстная реклама",
                    "Ищите сплит каналов для стабильного лидгена? Нет ничего надежнее классики!",
                    "40%",
                ],
            },
            {
                src: "/img/detection-card.png",
                gradient: "linear-gradient(180deg, rgba(51, 51, 51, 0) 0%, #333333 86.8%)",
                header: "Стабильная лидогенерация в кризис",
                text: [
                    "SEO-продвижение + Управление репутацией",
                    "Добавьте к классическому продвижению работу с профильными площадками и отзовиками.",
                    "40%",
                ],
            },
            {
                src: "/img/blocking-card.png",
                gradient: "linear-gradient(360deg, #333333 12.65%, rgba(51, 51, 51, 0) 97.54%)",
                header: "Стабильная лидогенерация в кризис",
                text: [
                    "SEO-продвижение + Таргет + Маркетплейсы",
                    "Основные каналы лидгена попали под блокировку? У нас уже есть работающее решение.",
                    "20%",
                ],
            }
        ]);
        return {
            cardItems,
        }
    },
}
</script>

<style scoped lang="scss">
.digital {
    display: flex;
    flex-direction: column;
    margin-top: 120px;
    margin: 0 200px;
    width: 100%;
}
.text {
    font-family: 'Montserrat';
    font-weight: 700;
    font-size: 38px;
    color: rgba(33, 33, 33, 1);
    line-height: 46px;
    .color-text {
        color: rgba(255, 89, 0, 1);
    }
}
.card-block {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
@media screen and (max-width: 1535px) {
    .card-block {
        justify-content: start;
    }
}
</style>