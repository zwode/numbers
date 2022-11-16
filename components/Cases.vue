<template>
  <div class="block-std container" id="case">
    <div class="block-title">
      Портфолио
    </div>
    <div class="d-flex flex-wrap mob-between">
      <div class="case" @click="openBlock(1)">
        <div class="d-flex justify-content-between">
          <div>
            Курсы и образование
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case" @click="openBlock(2)">
        <div class="d-flex justify-content-between">
          <div>
            Ремонт и строительство
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case" @click="openBlock(3)">
        <div class="d-flex justify-content-between">
          <div>
            IT продукты и сервисы
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case" @click="openBlock(4)">
        <div class="d-flex justify-content-between">
          <div>
            E-commerce
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case" @click="openBlock(5)">
        <div class="d-flex justify-content-between">
          <div>
            Оффлайн коммерция
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case" @click="openBlock(6)">
        <div class="d-flex justify-content-between">
          <div>
            Банки
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
    </div>
    <div class="cases animation-open">
      <OpenCase :block="numberCase"/>
    </div>
  </div>
</template>

<script>
import OpenCase from "./OpenCase";
export default {
  name: 'Case',
  data() {
    return {
      numberCase: null
    }
  },
  components: {OpenCase},
  methods: {
    openBlock (index) {
      document.querySelector('.cases').classList.add('animation-open')
      setTimeout(() => {
        const cases = document.querySelectorAll('.case')
        cases.forEach(el => el.classList.remove('active-case'))
        cases[index - 1].classList.add('active-case')
        this.numberCase = index
        document.querySelector('.cases').classList.remove('animation-open')
      }, 300)
    }
  }
}
</script>

<style scoped lang="scss">
.case {
  cursor: pointer;
  margin-bottom: 30px;
  margin-right: 30px;
  border: 1px solid #4c4c4c;
  padding: 20px;
  min-width: 350px;
  color: #000;
  background: #fff;
}

.case:hover {
  background: linear-gradient(114.93deg, rgba(111, 81, 210, 0.35) 0%, rgba(0, 0, 0, 0) 66.44%), linear-gradient(258.39deg, #15185B -6.72%, #000000 100%);
  color: #fff;
  img {
    filter: invert(98%) sepia(60%) saturate(0%) hue-rotate(186deg) brightness(108%) contrast(101%);
  }
}

.active-case {
  background: linear-gradient(114.93deg, rgba(111, 81, 210, 0.35) 0%, rgba(0, 0, 0, 0) 66.44%), linear-gradient(258.39deg, #15185B -6.72%, #000000 100%);
  color: #fff;
  img {
    filter: invert(98%) sepia(60%) saturate(0%) hue-rotate(186deg) brightness(108%) contrast(101%);
  }
}

.animation-open {
  opacity: 0;
}

.case:nth-child(3) {
  margin-right: 0;
}


.case:last-child {
  margin-right: 0;
}

@media (max-width: 768px) {
  .case {
    width: 100%;
    min-width: 0;
    max-width: 160px;
    padding: 5px 10px;
    margin-right: 0;
  }

  .mob-between {
    justify-content: space-between;
  }

  .case img {
    display: none;
  }
}
</style>
