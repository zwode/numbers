<template>
  <div class="d-flex justify-content-between flex-wrap">
    <div class="open-case d-flex" v-for="item in cases" v-if="item.block === block">
      <div class="open-case-gradient d-flex justify-content-center" :style="'background:' + item.background">
        <div class="open-case-img">
          <img :src="item.img" alt="image">
        </div>
      </div>
      <div class="open-case-description w-100">
        <ul>
          <li class="mt-3" v-for="list in item.description">
            {{ list }}
          </li>
        </ul>
      </div>
<!--      <a href="#price">-->
<!--        <div class="case-button">-->
<!--          <div class="price-button">-->
<!--            Перейти-->
<!--          </div>-->
<!--          <div class="button-arrow">-->
<!--            <img src="../assets/img/arrow-right.svg">-->
<!--          </div>-->
<!--        </div>-->
<!--      </a>-->
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
          background: 'linear-gradient(210.46deg, #FFDD33 -1.96%, rgba(0, 163, 76, 0.86) 59.44%, #8AC1F0 115.22%);',
          block: 1
        },
        {
          img: require('../assets/img/InterStudent.png'),
          description: ['200+ участников на платный марафон', '400+ участников на благотворительный марафон', 'Помощь в разработке основного сайта'],
          background: 'linear-gradient(210.46deg, #D9A763 -1.96%, #283340 59.44%, #8AC1F0 115.22%);',
          block: 1
        },
        {
          img: require('../assets/img/Ken.png'),
          description: ['ROMI более 10700%', 'Помощь в разработке основного сайта', 'Помощь в интеграции CRM системы'],
          background: 'linear-gradient(210.46deg, #005A66 -1.96%, #FABF5D 74.57%);',
          block: 2
        },
        {
          img: require('../assets/img/leroy.svg'),
          description: ['ROMI более 10700%', 'Помощь в разработке основного сайта', 'Помощь в интеграции CRM системы'],
          background: 'linear-gradient(210.46deg, #66C05D -1.96%, #283340 69.88%, #8AC1F0 115.22%);',
          block: 2
        },
        {
          img: require('../assets/img/flow.svg'),
          description: ['ROMI более 330%', 'Снижение стоимости лида в 2,48 раз', 'Помощь в разработке основного сайта'],
          background: 'linear-gradient(210.46deg, #1C1163 -1.96%, #8AC1F0 115.22%);',
          block: 3
        },
        {
          img: require('../assets/img/alif.png'),
          description: ['Более 2000 конверсий (продаж) на сайте', 'Стоимость конверсии от 0.7$', 'Увеличение доли покупателей среди посетителей сайта'],
          background: 'linear-gradient(224.19deg, #FFDD33 -1.02%, #8AC1F0 103.47%);',
          block: 4
        },
        {
          img: require('../assets/img/convex.png'),
          description: ['Изменение CJM', 'Запуск рекламной кампании с целью Brand Awareness'],
          background: 'linear-gradient(210.46deg, #00622B -1.96%, #283340 80.19%);',
          block: 4
        },
        {
          img: require('../assets/img/yes.png'),
          description: ['ROMI более 680%', 'Снижение стоимости лида в 1,7 раз', 'Изменение CJM'],
          background: 'linear-gradient(208.3deg, #FF9CCC -2.11%, #000000 153.69%);',
          block: 5
        },
        {
          img: require('../assets/img/bank.png'),
          description: ['Незначительное перевыполнение KPI по кликам, лидам и просмотрам', 'Аналитика рекламных кампаний', 'Оптимизация рекламных кампаний'],
          background: 'linear-gradient(208.3deg, #009B9B -2.11%, #000000 153.69%);',
          block: 6
        },
      ]
    }
  }
}
</script>

<style scoped>

li::marker {
  background: #44B591;
  color: #44B591;
  width: 16px!important;
  height: 16px!important;
  font-size: 16px;
}

li {
  color: #234D97;
  font-size: 20px;
}

.open-case-description {
  padding: 60px;
}
.open-case-img {
  background: #ffffff;
  padding: 35px;
  border-radius: 15px;
}

.open-case-gradient {
  width: 100%;
  padding: 100px 60px;
  border-radius: 30px;
}

.open-case {
  width: 100%;
  background: #fff;
  border-radius: 30px;
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

@media (max-width: 425px) {
  .open-case-gradient {
    border-radius: 15px;
  }
  .open-case {
    border-radius: 15px;
  }
  .open-case-description {
    padding: 0 60px;

  }

  li {
    font-size: 16px;
  }

  .justify-content-between {
    justify-content: center!important;
  }
}

</style>
