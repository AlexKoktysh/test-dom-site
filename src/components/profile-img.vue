<template>
   <div class="text-img">
        <div class="start-text">Комплексный интернет маркетинг</div>
        <div class="bottom-text">Мы помогаем бизнесу находить клиентов быстрее, интегрируруя маркетинговые, обучающие и технологические продукты</div>
        <div class="btn-block">
            <v-btn class="first-btn" color="#FF5900">Заказать увеличение продаж</v-btn>
            <v-btn class="second-btn" color="rgba(255, 255, 255, 0.2)">Заказать экспертный аудит</v-btn>
        </div>
    </div> 
</template>

<style scoped lang="scss">
.text-img {
    display: flex;
    flex-direction: column;
    width: 780px;
    height: 150px;
    margin-top: 170px;
    margin-left: 12.5%;
    font-family: 'Montserrat';
    color: #FFFFFF;
    .start-text {
        font-weight: 700;
        font-size: 68px;
        line-height: 74.8px;
    }
    .bottom-text {
        margin-top: 28px;
        margin-bottom: 52px;
        font-weight: 500;
        font-size: 16px;
        line-height: 22.4px;
    }
    .btn-block {
        .first-btn {
            border-radius: 100px;
            width: 362px;
            height: 62px;
            margin-right: 32px;
        }
        .second-btn {
            border-radius: 100px;
            width: 341px;
            height: 62px;
            border: 1px solid rgba(255, 255, 255, 1);
        }
    }
}
.second-btn {
    ::v-deep {
        .v-btn__content {
            text-transform: initial;
        }
    }
}
.first-btn {
    ::v-deep {
        .v-btn__content {
            text-transform: initial;
        }
    }
}
</style>