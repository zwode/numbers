<template>
  <div class="block-std">
    <div class="block-title">
      Папки и кейсы
    </div>
    <div class="d-flex flex-wrap">
      <div class="case">
        <div class="d-flex justify-content-between">
          <div>
            Курсы и образование
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case">
        <div class="d-flex justify-content-between">
          <div>
            Ремонт и строительство
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case">
        <div class="d-flex justify-content-between">
          <div>
            IT продукты и сервисы
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case">
        <div class="d-flex justify-content-between">
          <div>
            E-commerce
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
      <div class="case">
        <div class="d-flex justify-content-between">
          <div>
            Оффлайн коммерция
          </div>
          <div>
            <img src="../assets/img/plus.svg">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Case'
}
</script>

<style scoped>
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
  transition: all 0.3s ease;
  background: linear-gradient(114.93deg, rgba(111, 81, 210, 0.35) 0%, rgba(0, 0, 0, 0) 66.44%), linear-gradient(258.39deg, #15185B -6.72%, #000000 100%);
  color: #fff;
}

img .case:hover {
  filter: invert(98%) sepia(60%) saturate(0%) hue-rotate(186deg) brightness(108%) contrast(101%);
}

.case:nth-child(3) {
  margin-right: 0;
}
</style>
