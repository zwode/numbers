<template>
  <div class="block-std" id="price">
    <div class="block-title mb-text-align-center">
      Услуги и прайс
    </div>
    <div class="block-line d-none d-sm-block" />
    <div class="d-flex justify-content-between flex-wrap price-block">
      <img class="w-49 price-svg" style="margin-top: -10px" src="../assets/img/target.svg" alt="" v-b-modal.form-send>
      <img class="w-49 price-svg" src="../assets/img/ads.svg" alt="" v-b-modal.form-send>
      <img class="price-svg mt-2" style="width: 56%" src="../assets/img/bots.svg" alt="" v-b-modal.form-send>
      <img class="price-svg mt-2" style="width: 42%" src="../assets/img/constaling.svg" alt="" v-b-modal.form-send>
      <img class="w-49 price-svg mt-3" src="../assets/img/create.svg" alt="" v-b-modal.form-send>
      <img class="w-49 price-svg mt-3" src="../assets/img/smm.svg" alt="" v-b-modal.form-send>
    </div>
    <div>
      <img class="mt-5 w-100" src="../assets/img/brif.svg" alt="">
    </div>
    <div class="d-flex justify-content-center">
      <div class="button-send" v-b-modal.form-send>
        Обсудить проект
      </div>
    </div>
<!--    <div class="d-flex justify-content-between flex-wrap">-->
<!--      <div class="case-price" v-for="item in cases">-->
<!--        <div class="case-title">-->
<!--          {{ item.title }}  <span> {{ item.span }}</span>-->
<!--        </div>-->
<!--        <div class="case-description">-->
<!--          {{ item.description }}-->
<!--        </div>-->
<!--        <div class="case-button cursor-pointer" v-b-modal.form-send>-->
<!--          <div class="price-button">-->
<!--            {{ item.price }}-->
<!--          </div>-->
<!--          <div class="button-arrow">-->
<!--            <img src="../assets/img/arrow-right.svg">-->
<!--          </div>-->
<!--        </div>-->
<!--      </div>-->
<!--      <div class="case-price custom-case">-->
<!--        <div class="case-description">-->
<!--          Вы заполняете бриф на сайте.<br>-->
<!--          Созваниваемся и подробно обсуждаем все детали.<br>-->
<!--          Отправляем на утверждение.-->
<!--        </div>-->
<!--        <div class="custom-button cursor-pointer" v-b-modal.form-send>-->
<!--          <div class="price-button">-->
<!--            Обсудить проект-->
<!--          </div>-->
<!--          <div class="button-arrow">-->
<!--            <img src="../assets/img/Line.svg">-->
<!--          </div>-->
<!--        </div>-->
<!--      </div>-->
<!--    </div>-->
  </div>
</template>

<script>
export default {
  data() {
    return {
      block: [
        {
          img: require('~/assets/img/target.svg')
        },
        {
          img: require('~/assets/img/ads.svg')
        }
      ],
      cases: [
        {
          title: 'Таргетированная реклама',
          span: '(FB / TikTok)',
          description: 'Разработка, запуск, аналитика и оптимизация рекламы в Instagram, Facebook и TikTok',
          price: '9.990 тг'
        },
        {
          title: 'Контекстная реклама',
          span: '(Google Ads / Yandex)',
          description: 'Поисковая и баннерная реклама в рекламных сетях Google и Яндекс',
          price: '9.990 тг'
        },
        {
          title: 'Разработкачат-ботов\n',
          span: ' ',
          description: 'Автоматизация общения с потенциальными клиентами, раздача материалов через чат, массовые рассылки и многое другое',
          price: '9.990 тг'
        },
        {
          title: 'Создание сайтов',
          span: ' ',
          description: 'От разработки дизайна, до полноценной реализации многостраничного сайта или интернет-магазина\n',
          price: '9.990 тг'
        },
        {
          title: 'Консультации',
          span: ' ',
          description: 'Продвигаете свой бизнес самостоятельно? Получите концентрат знаний и опыта от специалиста в формате консультации. Решите свои вопросы, проверьте своих подрядчиков и вперёд к новым высотам!',
          price: '9.990 тг'
        }
      ]
    }
  }
}
</script>

<style scoped>

.button-send {
  margin-top: 6rem;
  padding: 15px 80px;
  background: #8AC1F0;
  border-radius: 18px;
  border: 2px solid #234D97;
  font-size: 36px;
  text-align: center;
  font-weight: bold;
  color: #ffffff;
  cursor: pointer;
  margin-bottom: 6rem;
}

.price-svg {
  cursor: pointer;
}

.case-price {
  max-width: 350px;
  max-height: 350px;
  width: 100%;
  border:  1px solid #C3C3C3;
  padding: 35px 20px 35px 40px;
  margin-bottom: 30px;
}

.w-49 {
  width: 49%;
}

.custom-case {
  padding: 0;
  border: 0;
  background: #373982;
  color: #ffffff;
}

.custom-case .case-description {
  margin-bottom: 80px;
  padding: 35px 20px 0 40px;
}

.custom-button {
  padding: 53px;
  border-top: 1px solid #ffffff;
  display: flex;
  justify-content: space-between;
}

.case-title {
  min-height: 56px;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  margin-bottom: 15px;
  max-width: 230px;
}

.case-title span {
  font-weight: 300;
}

.case-description {
  min-height: 140px;
  font-size: 16px;
  line-height: 18px;
}

.case-button {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  border: 1px solid black;
  max-width: 215px;
  padding: 20px 25px;
}

@media (max-width: 768px) {
  .case-description {
    min-height: auto;
    margin-bottom: 30px;
  }

  .case-price {
    max-height: 400px;
  }
}

@media (max-width: 425px) {
  .price-block {
    margin-left: -20px;
    margin-right: -20px;
  }
}

</style>
