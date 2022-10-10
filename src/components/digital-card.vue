<template>
    <Wrapper class="wrapper pt-15 pr-6" :srcImg="srcImg">
        <v-card width="360" height="487">
            <div class="content">
                <h3 class="text header">{{cardItem.header}}</h3>
                <v-divider color="#FFFFFF" />
                <p class="py-5 text">{{cardItem.text[0]}}</p>
                <v-divider color="#FFFFFF" />
                <p class="pt-5 text question-text">{{cardItem.text[1]}}</p>
                <p class="pt-7 text">Специальная скидка до <span class="span-item">{{cardItem.text[2]}}</span> на каждую услугу в пакете</p>
                <v-btn class="button mt-9" width="296" height="52">Приобрести пакет</v-btn>
            </div>
        </v-card>
    </Wrapper>
</template>

<script>
import styled from "vue3-styled-components";
import { ref } from "vue";
const WrapperProps = {
    srcImg: Object,
};
const Wrapper = styled("div", WrapperProps)`
.v-card {
    background: url(${({ srcImg }) => (srcImg.src)});
    background-size: cover !important;
    background-position-x: ${({ srcImg }) => (srcImg.position)}% !important;
    backdrop-filter: blur(1px);
    .content {
        background: ${({ srcImg }) => (srcImg.gradient)};
    }
}
`;
export default {
    components: {
        Wrapper,
    },
    props: {
        cardItem: Object,
    },
    setup(props) {
        const srcImg = ref({src: props.cardItem.src, gradient: props.cardItem.gradient, position: props.cardItem.position});
        return {
            srcImg,
        }
    },
}
</script>

<style scoped lang="scss">
.content {
    width: 360px;
    height: 487px;
    padding: 40px 32px 28px;
    .text {
        font-family: 'Montserrat';
        font-weight: 500;
        font-size: 16px;
        line-height: 22.4px;
        color: #FFFFFF;
    }
    .header {
        font-weight: 700;
        font-size: 18px;
        line-height: 25.2px;
        letter-spacing: 0.01em;
        text-transform: uppercase;
        margin-bottom: 28px;
    }
    .span-item {
        font-size: 18px;
        font-weight: 800;
        line-height: 25px;
        letter-spacing: 0em;
    }
    .question-text {
        font-size: 14px;
        font-weight: 500;
        line-height: 20px;
        letter-spacing: 0em;
        opacity: 0.5;
    }
    .button {
        border-radius: 100px;
        border: 1px solid #FF5900;
        background-color: transparent;
        ::v-deep {
            .v-btn__content {
                text-transform: initial;
                color: #FF5900;
                font-family: 'Montserrat';
                font-style: normal;
                font-weight: 500;
                font-size: 16px;
                line-height: 20px;
            }
        }
    }
}
.v-divider {
    opacity: 20%;
}
</style>