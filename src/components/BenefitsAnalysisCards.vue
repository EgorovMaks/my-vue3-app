<template>
  <div class="benefits-cards">
    <h2 class="benefits-cards__title">Плюсы использования сервиса «Компас» для анализа штрафов</h2>
    <div class="benefits-cards__container ">
      <div v-for="(card, index) in cardsBenefits" :key="index" class="benefits-card__wrap">
        <iconsCard :type="card.img"/>
        <div class="benefits-card__text-wrap">
          <h3 class="benefits-card__title blue-text">
            {{ card.title }}
          </h3>
          <p class="benefits-card__text">
            {{ card.text }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import iconsCard from './icons/iconsCard.vue'
export default {
  components: {
    iconsCard,
  },
  data() {
    return {
      cardsBenefits: [
        { img:'infinitely', title: 'Неограниченый автопарк', text: 'Можно добавить неограниченное кол-во машин и водителей', },
        {img:'card', title: 'Сокращение затрат до 50%', text: 'Максимально быстро узнаете о штрафах в автоматическом режиме, тем самым у вас есть время оплатить по скидке',  },
        {img:'shield', title: 'Безопасность', text: 'Данные передаются в зашифрованном виде, они доступны только получателю',  },
        {img:'bell', title: 'Уведомление о погашении', text: 'Мы оповестим вас о том, что штраф был погашен и соответствующая запись создана в ГИС ГМП',  },
        {img:'receipt', title: 'Квитанция об оплате', text: 'После совершения оплаты банковской картой на Вашу электронную почту придет квитанция об успешной оплате.',  },
        {img:'time', title: 'Все история сохраняется по каждой машине', text: 'Вся история штрафов сохраняется по машине и водителю, позволяет анализировать статистику по штрафам',  },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
    .benefits-cards{
        --site-width-cards: 1156px;
        width: var(--site-width-cards);
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 98px;
        &__title{
            font-weight: 700;
            font-size: 2.12rem;
            line-height: 120%;
            color: #000;
            transform: translateX(-11px);
            margin-bottom: 37px;
        }
        &__container{
          display: grid;
          width: 100%;
          grid-template-columns: repeat(6, 1fr);
          gap: 35px;
        }
    }
    .benefits-card{
        &__wrap{
          display: flex;
          align-items: center;
          gap: 15px;
          grid-column: span 2;
          background: #fbfcfd;
          border: 1px solid #eeeff1;
          border-radius: 0.62rem;
          padding: 24px  16px;
        }
        &__text-wrap{
          max-width: 254px;
        }
        &__title{
          font-weight: 700;
            font-size: 1.12rem;
            line-height: 120%;
            margin-bottom: 10px;
        }
        &__text{
          font-size: 0.94rem;
          line-height: 120%;
          color: #000;
        }
      
    }
</style>