<template>
    <div class="basement">
        <div class="text-block">
            <h3 class="header">Найдем клиентов в Интернете для Вас</h3>
            <p class="item mt-10">
                Для заказа стратегии продвижения в Москве или другом городе просто заполни заявку или закажи обратный звонок. Менеджер по работе с клиентами выйдет на связь и подготовит персональное коммерческое предложение, составленное с учетом желаемых целей и возможностей.
            </p>
            <v-form class="mt-10">
                <v-container>
                    <v-text-field
                        label="Имя"
                        width="510"
                        bg-color="#F4F4F4"
                    ></v-text-field>
                    <v-text-field
                        label="E-mail"
                        width="510"
                        bg-color="#F4F4F4"
                    ></v-text-field>
                    <v-checkbox class="checkbox" label="Я даю свое согласие на обработку персональных данных"></v-checkbox>
                    <v-btn color="#FF5900" class="btn-send">Отправить заявку</v-btn>
                </v-container>
            </v-form>
        </div>
    </div>
    <div class="bottom">
        <div class="bottom-block">
            <div class="info">
                <div class="logo">
                    <v-img contain width="42.96" height="48" src="/img/logo-bottom.svg"></v-img>
                    <div class="logo-content">
                        <div class="text top-text-logo">ДОМ САЙТОВ</div>
                        <div class="text bottom-text-logo">УВЕЛИЧЕНИЕ ПРОДАЖ</div>
                    </div>
                </div>
                <div class="region mb-5">
                    <div class="text-region">Ваш регион: </div>
                    <div class="content-region">Тула</div>
                </div>
                <div class="contact mb-3">
                    +7 (495) 223-66-59 г. Тула, ул. Пушкинская, 27
                </div>
                <div class="unp mb-7">
                    <p>ИНН 123456789</p>
                    <p>ОГРН 123456789010</p>
                </div>
                <div class="social">
                    <v-img contain width="40" height="40" src="/img/vk.svg"></v-img>
                    <v-img class="ml-5" contain width="40" height="40" src="/img/tg.svg"></v-img>
                </div>
            </div>
            <div class="business-block">
                <div class="header mb-6">УВЕЛИЧЕНИЕ ПРОДАЖ ДЛЯ ВАШЕГО БИЗНЕСА</div>
                <div class="content" v-for="(item, i) in businessBlock" :key="i">{{item}}</div>
            </div>
            <div class="development-block">
                <div class="header mb-6">РАЗРАБОТКА И ПОДДЕРЖКА САЙТОВ</div>
                <div class="content" v-for="(item, i) in developmentBlock" :key="i">{{item}}</div>
            </div>
            <div class="company-block">
                <div class="header mb-6">КОМПАНИЯ «ДОМ САЙТОВ»</div>
                <div class="content" v-for="(item, i) in companyBlock" :key="i">{{item}}</div>
            </div>
        </div>
        <div class="label">
            <div>© 2008-2022 Компания «ДОМ САЙТОВ»</div>
            <div>Карта сайта | Политика конфиденциальности</div>
        </div>
    </div>
    <v-divider />
</template>

<script>
export default {
    setup() {
        const businessBlock = [
            "SEO",
            "Тариф «Трафик»",
            "Тариф «Объем работ»",
            "Тариф «Лиды / CPA»",
            "Тариф «SEO + Контекст»",
            "Комплексное SEO",
            "Для интернет-магазина",
            "Продвижение в Яндекс",
            "Продвижение в Google",
            "Разовые работы",
            "SEO-аудит сайтов",
            "Вывод из-под санкций",
        ];
        const developmentBlock = [
            "Разработка",
            "На 1С-Битрикс",
            "На WordPress",
            "На Tilda",
            "Сайт-визитка",
            "Интернет-магазин",
            "Проектирование",
            "Поддержка сайтов",
            "Внесение дорабток",
        ];
        const companyBlock = [
            "Клиенты и отзывы",
            "Контакты",
            "Работа в Demis Group",
            "Личный кабинет",
            "Статьи",
            "Публичная оферта",
            "Партнерская программа",
            "Гарантии",
            "Внесение дорабток",
        ];
        return {
            businessBlock,
            developmentBlock,
            companyBlock,
        }
    },
}
</script>

<style scoped lang="scss">
.basement {
    height: 789px;
    background: url("/public/img/basement.png"), linear-gradient(90deg, rgba(0, 0, 0, 0.25) 0%, rgba(0, 0, 0, 0.025) 62.79%);
    backdrop-filter: blur(1px);
    transform: matrix(-1, 0, 0, 1, 0, 0);
    background-size: cover;
    background-position-y: 40%;
    .text-block {
        height: 789px;
        transform: inherit;
        color: #FFFFFF;
        font-family: 'Montserrat';
        background: linear-gradient(90deg, rgba(0, 0, 0, 0.25) 0%, rgba(0, 0, 0, 0.025) 62.79%);
        margin-top: 120px;
        .header {
            padding-top: 120px;
            font-style: normal;
            font-weight: 700;
            font-size: 38px;
            line-height: 120%;
            margin-left: 346px;
        }
        .item {
            height: 66px;
            width: 908px;
            text-align: center;
            margin-left: 320px;
            font-size: 16px;
            font-weight: 500;
            line-height: 22px;
            letter-spacing: 0em;
        }
        .v-form {
            margin-left: 485px;
            height: 357px;
            width: 630px;
            border-radius: 0px;
            background-color: #F4F4F4;
            color: rgba(51, 51, 51, 0.5);
            display: flex;
            justify-content: center;
        }
    }
    .v-text-field::v-deep {
        .v-input__control {
            width: 95%;
        }
        .v-label {
            font-size: 16px;
            font-family: 'Montserrat';
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 100%;
            color: #333333;
            opacity: 0.4;
        }
    }
    .v-checkbox::v-deep {
        .v-label {
            font-size: 14px;
            font-family: 'Montserrat';
            font-style: normal;
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #212121 !important;
        }
    }
    .btn-send {
        padding: 20px 40px;
        gap: 10px;
        width: 250px;
        height: 62px;
        backdrop-filter: blur(2.5px);
        border-radius: 100px;
        box-shadow: none;
        ::v-deep {
            .v-btn__content {
                font-family: 'Montserrat';
                font-style: normal;
                font-weight: 500;
                font-size: 18px;
                line-height: 22px;
                color: #FFFFFF;
                flex: none;
                order: 0;
                flex-grow: 0;
                text-transform: initial;
            }
        }
    }
    .v-container {
        width: 93%;
    }
}
.bottom {
    height: 583px;
    background-color: #333333;
    .bottom-block {
        height: 532px;
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        padding: 100px 200px 0;
        .info {
            width: 16%;
            .logo {
                display: flex;
                flex-direction: row;
                width: 185px;
                height: 48px;
                margin-bottom: 57px;
                .logo-content {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    margin-left: 13.24px;
                }
            }
            .text {
                font-family: 'Montserrat';
                color: #FFFFFF;
                font-weight: 500;
                line-height: 17px;
                text-transform: uppercase;
            }
            .top-text-logo {
                font-size: 16px;
            }
            .bottom-text-logo {
                font-size: 8.5px;
                opacity: 0.3;
            }
            .region {
                display: flex;
                flex-direction: row;
                align-items: center;
                .text-region {
                    font-family: 'Montserrat';
                    font-style: normal;
                    font-weight: 500;
                    font-size: 14px;
                    line-height: 170%;
                    color: #FFFFFF;
                    opacity: 0.5;
                }
                .content-region {
                    font-family: 'Montserrat';
                    font-style: normal;
                    font-weight: 500;
                    font-size: 14px;
                    line-height: 100%;
                    color: #FFFFFF;
                    text-decoration: underline;
                }
            }
            .contact {
                font-family: 'Montserrat';
                font-style: normal;
                font-weight: 500;
                font-size: 14px;
                line-height: 170%;
                color: #FFFFFF;
            }
            .unp {
                font-family: 'Montserrat';
                font-style: normal;
                font-weight: 500;
                font-size: 14px;
                line-height: 170%;
                color: #FFFFFF;
                opacity: 0.5;
            }
            .social {
                display: flex;
                flex-direction: row;
                .v-responsive {
                    flex: none;
                }
            }
        }
        .business-block {
            width: 17%;
        }
        .development-block {
            width: 17%;
        }
        .company-block {
            width: 14%;
        }
        .header {
            font-family: 'Montserrat';
            font-style: normal;
            font-weight: 500;
            font-size: 14px;
            line-height: 140%;
            color: #FFFFFF;
            opacity: 0.5;
            flex: none;
            order: 0;
            flex-grow: 0;
        }
        .content {
            font-family: 'Montserrat';
            font-style: normal;
            font-weight: 500;
            font-size: 14px;
            line-height: 170%;
            color: #FFFFFF;
            flex: none;
            order: 1;
            flex-grow: 0;
        }
    }
    .label {
        display: flex;
        justify-content: space-between;
        margin: 20px 200px 16px;
        font-family: 'Montserrat';
        font-style: normal;
        font-weight: 500;
        font-size: 12px;
        line-height: 120%;
        color: #FFFFFF;
        opacity: 0.3;
    }
}
.v-divider {
    position: absolute;
    bottom: 50px;
    width: 1200px;
    background-color: #FFFFFF;
    opacity: 0.1;
    margin: 0 200px;
}
</style>