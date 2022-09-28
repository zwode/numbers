<template>
  <div class="d-flex justify-content-between flex-wrap">
    <div class="open-case" v-for="item in cases" v-if="item.block === block">
      <div class="">
        <img :src="item.img" alt="image">
      </div>
      <ul class="" v-for="list in item.description">
        ⎯  &nbsp; {{ list }}
      </ul>
      <a href="#price">
        <div class="case-button">
          <div class="price-button">
            Перейти
          </div>
          <div class="button-arrow">
            <img src="../assets/img/arrow-right.svg">
          </div>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'OpenCase',
  props: ['block'],
  data() {
    return {
      cases: [
        {
          img: require('~/assets/img/finmentor.svg'),
          description: ['1000+ участников в онлайн выставке зарубежного образования', '300+ лидов ежемесячно', 'Помощь в разработке дополнительного сайта'],
          block: 1
        },
        {
          img: require('../assets/img/InterStudent.png'),
          description: ['200+ участников на платный марафон', '400+ участников на благотворительный марафон', 'Помощь в разработке основного сайта'],
          block: 1
        },
        {
          img: require('../assets/img/Ken.png'),
          description: ['ROMI более 10700%', 'Помощь в разработке основного сайта', 'Помощь в интеграции CRM системы'],
          block: 2
        },
        {
          img: require('../assets/img/leroy.svg'),
          description: ['ROMI более 10700%', 'Помощь в разработке основного сайта', 'Помощь в интеграции CRM системы'],
          block: 2
        },
        {
          img: require('../assets/img/flow.svg'),
          description: ['ROMI более 330%', 'Снижение стоимости лида в 2,48 раз', 'Помощь в разработке основного сайта'],
          block: 3
        },
        {
          img: require('../assets/img/alif.png'),
          description: ['Более 2000 конверсий (продаж) на сайте', 'Стоимость конверсии от 0.7$', 'Увеличение доли покупателей среди посетителей сайта'],
          block: 4
        },
        {
          img: require('../assets/img/convex.png'),
          description: ['Изменение CJM', 'Запуск рекламной кампании с целью Brand Awareness'],
          block: 4
        },
        {
          img: require('../assets/img/yes.png'),
          description: ['ROMI более 680%', 'Снижение стоимости лида в 1,7 раз', 'Изменение CJM'],
          block: 5
        },
        {
          img: require('../assets/img/bank.png'),
          description: ['Незначительное перевыполнение KPI по кликам, лидам и просмотрам', 'Аналитика рекламных кампаний', 'Оптимизация рекламных кампаний'],
          block: 6
        },
      ]
    }
  }
}
</script>

<style scoped>
.open-case {
  padding: 40px;
  border: 1px solid #000000;
  max-width: 540px;
  width: 100%;
  margin-top: 30px;
}

.open-case a {
  color: #000000;
}

.open-case ul {
  font-size: 16px;
  padding: 0;
}

.open-case img {
  margin-bottom: 80px;
}

.case-button {
  margin-top: 40px;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  border: 1px solid black;
  max-width: 100%;
  padding: 13px 25px;
  height: 50px;
}
</style>
