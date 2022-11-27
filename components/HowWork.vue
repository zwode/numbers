<template>
  <div class="block-std" id="work">
    <div class="block-title">
      Принципы работы
    </div>
    <div class="d-flex justify-content-between flex-wrap">
      <div class="card d-flex" @click="isActive = !isActive" :class="{ 'active-card': isActive }">
        <div class="card-body overflow-hidden d-flex" :class="{ 'hidden': isActive }">
          <img src="../assets/img/worktogether.svg" alt="" width="100px" height="100px" class="card-icon">
          <div class="card-title">
            Совместная<br>
            работа
          </div>
        </div>
        <div class="card-text" :class="{ 'hidden': !isActive }">
            <span>
              Наши заказчики могут проверить ход работы на любом из её этапов, а не только после отчётного периода.
            </span>
        </div>
      </div>

      <div class="card d-flex" @click="isActive1 = !isActive1" :class="{ 'active-card': isActive1 }">
        <div class="card-body overflow-hidden d-flex" :class="{ 'hidden': isActive1 }">
          <img src="../assets/img/limitclient.svg" alt="" width="100px" height="100px" class="card-icon">
          <div class="card-title">
            Ограниченное<br> количество
            клиентов
          </div>
        </div>
        <div class="card-text" :class="{ 'hidden': !isActive1 }">
          <span>
            Для достижения необходимых результатов мы обязаны сохранять фокус. Каждый специалист имеет свой порог количества проектов, который он ведёт. Это помогает достигнуть цели заказчика и защитить сотрудников от выгорания.
          </span>
        </div>
      </div>

      <div class="card d-flex" @click="isActive2 = !isActive2" :class="{ 'active-card': isActive2 }">
        <div class="card-body overflow-hidden d-flex" :class="{ 'hidden': isActive2 }">
          <img src="../assets/img/withClient.svg" alt="" width="100px" height="100px" class="card-icon">
          <div class="card-title">
            Глубокие<br> отношения
            с клиентом
          </div>
        </div>
        <div class="card-text" :class="{ 'hidden': !isActive2 }">
          <span>
            Чем лучше мы понимаем продукт или услугу заказчика, тем эффективнее нам удастся продвигать его. Мы будем рады принять участие не только в личных встречах с заказчиком, но и в его внутренней кухне
          </span>
        </div>
      </div>

      <div class="card d-flex" @click="isActive3 = !isActive3" :class="{ 'active-card': isActive3 }">
        <div class="card-body overflow-hidden d-flex" :class="{ 'hidden': isActive3 }">
          <img src="../assets/img/proactivantion.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Ответственность<br>
            и проактивность
          </div>
        </div>
        <div class="card-text" :class="{ 'hidden': !isActive3 }">
            <span>
              Готовых решений не существует. Два заказчика из одной ниши могут иметь совершенно разные пути продвижения. Мы готовы к вызовам.
            </span>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HowWork',
  data() {
    return {
      isActive: false,
      isActive1: false,
      isActive2: false,
      isActive3: false
    }
  },
  methods: {

  }
}
</script>
<style scoped>
.card-icon {
  align-self: center;
}
.open {
  background: linear-gradient(114.93deg, rgba(111, 81, 210, 0.35) 0%, rgba(0, 0, 0, 0) 66.44%), linear-gradient(258.39deg, #15185B -6.72%, #000000 100%);
}

.open span {
  background-color: #ffffff!important;
}

.open .arrow--l-r {
  background-color: transparent!important;
}

.card-text {
  color: #ffffff;
  padding: 20px;
  font-size: 20px;
}

.card-height {
  height: 195px;
}

.h-0 {
  height: 0!important;
  transition: height 0.15s ease-out;
}

.h-100 {
  transition: height 0.25s ease-out;
}

.card-title {
  margin-left: 20px;
  align-self: center;
  color: #234D97;
  font-weight: 500;
  font-size: 25px;
}
.card {
  cursor: pointer;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.93) 23.48%, rgba(121, 110, 110, 0) 363.5%);;
  border: 2px solid #234D97;
  border-radius: 30px;
  max-width: 540px;
  width: 100%;
  margin-bottom: 30px;
  flex-direction: row;
}

.active-card {
  background: linear-gradient(226.03deg, #234D97 34.36%, rgba(147, 167, 204, 0.81) 107.51%, rgba(255, 255, 255, 0.23) 178.61%);
}


.card-body {
  padding: 25px 40px;
}

.wrap {
  align-self: center;
}

.card-open {
  align-self: center;
}

@media (max-width: 425px) {
  .card-title {
    margin-bottom: 0!important;
    font-size: 16px!important;
  }
  .card-icon {
    width: 50px!important;
    height: 50px!important;
  }
}

</style>
