<template>
  <div class="d-flex justify-content-between w-100 nav-container">
    <div class="d-flex justify-content-center px-5 border-left-header">
      <div class="align-self-center">
        <img src="../assets/img/image.svg">
      </div>
    </div>
    <div class="d-flex text-white nav-text">
      <div class="nav-link">
        Главная
      </div>
      <div class="nav-link">
        Кейсы
      </div>
      <div class="nav-link">
        Принципы
      </div>
      <div class="nav-link">
        Услуги
      </div>
      <div class="nav-link">
        Контакты
      </div>
    </div>
    <a>
      <div class="btn-send w-100 text-black">
        Оставить заявку
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: 'NavHeader'
}
</script>

<style scoped>

  .text-black {
    color: black!important;
  }

  .btn-send {
    background: #fff;
    padding: 27.5px 50px;
    text-transform: uppercase;
  }

  .nav-text {
    color: #fff!important;
    align-self: center;
    border-top: 0;
    border-left: 0;
    height: 100%;
  }

  .nav-container {
    height: 80px;
  }

  .nav-link {
    align-self: center;
    cursor: pointer;
  }

  a {

  }

</style>
