<template>
    <div class="traffic-check">
        <form class="traffic-check__form form">
            <h1 class="form__title">{{ titleForm }}</h1>
            <div class="input-wrapper">
                <div class="form__input-car-number input-wrap">
                <label for="carNumber">Номер автомобиля</label>
                <input type="text" id="carNumber" name="carNumber" class="form__input" required>
            </div>
            <div class="form__input-region input-wrap">
                <label for="carNumber">Регион</label>
                <input type="text" id="carNumber" name="carNumber" class="form__input" required>
            </div>
            </div>
            <div class="form__input-certificate input-wrap">
                <label for="carNumber">Свидетельство о регистрации ТС</label>
                <input type="text" id="carNumber" name="carNumber" class="form__input" required>
            </div>
            <div class="input-wrapper">
                <BaseButton arrow="left" text="Проверить штрафы" class="form__input-btn-left"/>
                <button class="form__input-btn-right">
                    <YouTube/>
                    О сервисе
                    <span class="blue-text">(1 мин. 20 сек)</span>
                </button>
            </div>
            <p class="form-info">
                Нажимая «Проверить штрафы» вы соглашаетесь с политикой обработки персональных данных и принимаете оферту
            </p>
        </form>
        <div class="traffic-check__image-container">
            <img src="@/assets/images/form-image.jpg" alt="Ноутбук" class="form-image" />
        </div>
    </div>
</template>

<script>
import BaseButton from '../components/ui/BaseButton.vue';
import YouTube from './icons/YouTube.vue'
export default {
  components: {
    BaseButton,
    YouTube,
  },
  data() {
    return {
        titleForm: 'Проверьте штрафы и зарегестрируйтесь в 1 клик'
    };
  },
};
</script>

<style lang="scss" scoped>
    .traffic-check{
        --site-width-check: 1135px;
        width: var(--site-width-check);
        margin-top: 79px;
        display: flex;
        justify-content: space-between;
        margin-bottom: 102px;
        &__form{
            width: 50%;
        }
    }
    .form{
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-auto-rows: min-content;
        &__title{
            grid-column: span 6;
            font-family: var(--font-family);
            font-weight: 700;
            font-size: 2.56rem;
            line-height: 120%;
            color: #000;
            margin-bottom: 26px;
        }
        .input-wrapper{
            grid-column: span 6;
            display: flex;
            column-gap: 30px;
            margin-bottom: 16px;
        }
        &__input{
            &-car-number{
                flex-grow: 1
            }
            &-region{
                width: 38%;
            }
            &-certificate{
                grid-column: span 6;
                margin-bottom: 15px;
            }
            &-btn-left{
                width: 37%;
                padding-top: 11px;
                padding-bottom: 11px;
                font-size: 1.12rem;
                color: #fff;
            }
            &-btn-right{
                display: flex;
                justify-content: center;
                gap: 5px;
                align-items: center;
                border-radius: 0.44rem;
                border: 1px solid #0584fe; 
                padding: 11px 23px;
                span{
                    display: flex;
                    align-items: center;
                }
                .blue-text{
                    font-weight: 400;
                    font-size: 0.94rem;
                }
            }
        }
        &-info{
            grid-column: span 6;
            font-size: 0.81rem;
            line-height: 120%;
            color: #8f8f8f;
        }
    }
    .input-wrap{
        display: flex;
        flex-direction: column;
        label{
            font-family: var(--font-family);
            font-size: 0.75rem;
            line-height: 120%;
            color: #000;
            margin-bottom: 4px;
        }
        input{
            height: 40px;
            border: 1px solid #bcbcbc;
            border-radius: 0.31rem;
            width: 100%;
        }
    }
</style>