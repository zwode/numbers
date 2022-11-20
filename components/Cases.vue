<template>
  <div class="block-std container" id="case">
    <div class="block-title">
      Портфолио
    </div>
    <div class="d-flex flex-wrap mob-between">
      <div class="case" v-for="(inCase, index) in caseText" @click="openBlock(index + 1)">
        <div class="d-flex">
          <div class="mr-4 align-self-center">
            <img src="../assets/img/arrow-right.svg">
          </div>
          <div class="case-text">
            {{ inCase.text }}
          </div>
        </div>
      </div>
    </div>
    <div class="cases">
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
      numberCase: 1,
      caseText: [
        {
          text: 'Курсы и образование'
        },
        {
          text: 'Ремонт и строительство'
        },
        {
          text: 'IT- продукты и сервисы'
        },
        {
          text: 'E-commerce'
        },
        {
          text: 'Офлайн комммерция'
        },
        {
          text: 'Банки'
        }
      ]
    }
  },
  components: { OpenCase },
  mounted() {
    document.querySelector('.case').classList.add('active-case')
  },
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
  border: 1px solid transparent;
  padding: 15px;
  color: #000;
  background: #fff;
  border-radius: 15px;
}

.case:hover {
  color: #fff;
  border: 1px solid transparent;
  background: linear-gradient(94.33deg, #234D97 -12.22%, #7058D0 86.23%);
  img {
    filter: invert(98%) sepia(60%) saturate(0%) hue-rotate(186deg) brightness(108%) contrast(101%);
  }
}

.case-text {
  font-size: 20px;
}

.active-case {
  border: 1px solid transparent;
  background: linear-gradient(94.33deg, #234D97 -12.22%, #7058D0 86.23%);
  color: #fff;
  img {
    filter: invert(98%) sepia(60%) saturate(0%) hue-rotate(186deg) brightness(108%) contrast(101%);
  }
}

.animation-open {
  opacity: 0;
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
