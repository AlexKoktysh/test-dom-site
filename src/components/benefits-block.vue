<template>
    <div class="benefits-block">
        <h3 class="text header">Преимущества работы с нами</h3>
        <div class="card-block">
            <div v-for="(item, i) in itemsCard" :key="i">
                <v-card width="360" height="160">
                    <v-img contain width="70" height="70" :src="item.icon"></v-img>
                    <div class="text-card">{{item.text}}</div>
                </v-card>
            </div>
        </div>
    </div>
</template>

<script>
import { ref } from "vue";
export default {
    setup() {
        const itemsCard = ref([
            {
                text: "Увеличиваем продажи, звонки и заявки с Вашего сайта",
                icon: "/test-dom-site/img/increase-sales.svg",
            },
            {
                text: "Используем современные технологии и собственные разработки",
                icon: "/test-dom-site/img/modern-technologies.svg",
            },
            {
                text: "Всегда оправдываем ожидания наших Клиентов",
                icon: "/test-dom-site/img/customer-waiting.svg",
            },
            {
                text: "Более 100 благодарственных писем от Клиентов",
                icon: "/test-dom-site/img/letter-icon.svg",
            },
            {
                text: "Безупречная репутация на digital-рынке",
                icon: "/test-dom-site/img/reputation-icon.svg",
            },
            {
                text: "Помогаем достигать имиджевых и финансовых целей",
                icon: "/test-dom-site/img/achievements-goals-icon.svg",
            },
        ]);
        return {
            itemsCard,
        };
    },
}
</script>

<style scoped lang="scss">
.benefits-block {
    height: 466px;
    .card-block {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        .v-card {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: none;
        }
    }
    .text {
       font-family: Montserrat; 
    }
    .text-card {
        font-size: 16px;
        font-weight: 500;
        line-height: 22px;
        letter-spacing: 0em;
        color: #333333;
        font-style: normal;
        text-align: center;
    }
    .header {
        font-size: 38px;
        font-weight: 700;
        line-height: 46px;
        letter-spacing: 0em;
        color: #212121;
    }
}
</style>