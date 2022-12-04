<template>
  <div class="block-std container" id="case">
    <div class="block-title mb-padding">
      Портфолио
    </div>
    <div class="block-line" />
    <div class="d-flex flex-wrap mob-between">
      <div class="case" v-for="(inCase, index) in caseText" @click="openBlock(index + 1)">
        <div class="d-flex">
          <div class="mr-4 align-self-center">
            <img src="../assets/img/arrow-case.svg">
          </div>
          <div class="case-text">
            {{ inCase.text }}
          </div>
        </div>
      </div>
    </div>
    <div class="cases mb-scale-xs">
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

<style lang="scss">
.case {
  cursor: pointer;
  margin-bottom: 30px;
  margin-right: 30px;
  border: 1px solid transparent;
  padding: 15px;
  color: #000;
  background: #fff;
  border-radius: 15px;
  img {
    filter: invert(16%) sepia(91%) saturate(4944%) hue-rotate(253deg) brightness(94%) contrast(97%);
  }
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
    margin-right: 10px;
    max-width: max-content;
    padding: 5px 10px;
    margin-right: 0;
  }
  .card {
    border-radius: 15px!important;
  }
  .mob-between {
  }

  .case img {
  }
}

@media (max-width: 425px) {
  .mb-scale-xs {
    transform: scale(0.7);
    margin-top: -130px;
    margin-bottom: -130px;
  }
  .open-case-gradient {
    padding: 25px 60px!important;
  }

  .open-case {
    max-width: 350px;
    display: block!important;
  }
  .case-text {
    align-self: center;
  }

  .mob-between {
    padding: 10px;
  }

  .case {
    margin-bottom: 10px !important;
    border-radius: 10px !important;
    margin-right: 15px;
    .mr-4 {
      margin-right: 10px !important;
    }
  }
  .case img {
    width: 15px;
  }
  .case-text {
    font-size: 10px;
  }
}

</style>
