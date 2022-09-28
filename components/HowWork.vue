<template>
  <div class="block-std" id="work">
    <div class="block-title">
      Принципы работы
    </div>
    <div class="d-flex justify-content-between flex-wrap">
      <div class="card d-flex">
        <div class="card-body overflow-hidden" :class="{ 'card-height': !isActive, 'h-100': isActive }">
          <img src="../assets/img/worktogether.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Полная<br> прозрачность
          </div>
          <div class="card-text">
            <span>
              Наши заказчики могут проверить ход работы на любом из её этапов, а не только после отчётного периода.
            </span>
          </div>
        </div>
        <div class="card-open" @click="isActive = !isActive" :class="{ 'open': isActive }">
          <div class="wrap"><span class="arrow--l-r" :class="{ 'right': isActive, 'left': !isActive }"><span></span><span></span><span></span><span></span><span></span></span></div>
        </div>
      </div>

      <div class="card d-flex">
        <div class="card-body overflow-hidden" :class="{ 'card-height': !isActive1, 'h-100': isActive1 }">
          <img src="../assets/img/limitclient.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Ограниченное количество<br>
            клиентов
          </div>
          <div class="card-text">
            <span>
              Для достижения необходимых результатов мы обязаны сохранять фокус. Каждый специалист имеет свой порог количества проектов, который он ведёт. Это помогает достигнуть цели заказчика и защитить сотрудников от выгорания.
            </span>
          </div>
        </div>
        <div class="card-open"  @click="isActive1 = !isActive1" :class="{ 'open': isActive1 }">
          <div class="wrap"><span class="arrow--l-r" :class="{ 'right': isActive1, 'left': !isActive1 }"><span></span><span></span><span></span><span></span><span></span></span></div>
        </div>
      </div>

      <div class="card d-flex">
        <div class="card-body overflow-hidden" :class="{ 'card-height': !isActive2, 'h-100': isActive2 }">
          <img src="../assets/img/withClient.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Глубокие отношения<br>
            с клиентом
          </div>
          <div class="card-text">
            <span>
              Чем лучше мы понимаем продукт или услугу заказчика, тем эффективнее нам удастся продвигать его. Мы будем рады принять участие не только в личных встречах с заказчиком, но и в его внутренней кухне
            </span>
          </div>
        </div>
        <div class="card-open" :class="{ 'open': isActive2 }" @click="isActive2 = !isActive2">
          <div class="wrap"><span class="arrow--l-r" :class="{ 'right': isActive2, 'left': !isActive2 }" ><span></span><span></span><span></span><span></span><span></span></span></div>
        </div>
      </div>

      <div class="card d-flex">
        <div class="card-body overflow-hidden" :class="{ 'card-height': !isActive3, 'h-100': isActive3 }">
          <img src="../assets/img/proactivantion.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Ответственность<br>
            и проактивность
          </div>
          <div class="card-text">
            <span>
              Готовых решений не существует. Два заказчика из одной ниши могут иметь совершенно разные пути продвижения. Мы готовы к вызовам.
            </span>
          </div>
        </div>
        <div class="card-open" :class="{ 'open': isActive3 }" @click="isActive3 = !isActive3">
          <div class="wrap"><span class="arrow--l-r" :class="{ 'right': isActive3, 'left': !isActive3 }" ><span></span><span></span><span></span><span></span><span></span></span></div>
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
  margin-top: 40px;
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
  text-transform: uppercase;
}
.card {
  max-width: 540px;
  width: 100%;
  margin-bottom: 30px;
  flex-direction: row;
}

.card-body {
  padding: 25px 40px;
}

.wrap {
  align-self: center;
}

.card-open {
  cursor: pointer;
  display: flex;
  border-left: 0.5px solid rgba(0, 0, 0, 0.125);
  height: 100%;
  padding: 25px 0;
  align-self: center;
}

.card-icon {
  margin-bottom: 40px;
}
</style>
