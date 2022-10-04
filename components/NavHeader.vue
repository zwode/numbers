<template>
  <div>
    <div class="d-none d-lg-block">
      <div class="d-flex justify-content-between w-100 nav-container">
        <div class="d-flex justify-content-center px-5 border-left-header">
          <div class="align-self-center">
            <img src="../assets/img/logo.svg">
          </div>
        </div>
        <div class="d-flex text-white nav-text">
          <div class="nav-link">
            <a href="/">
              Главная
            </a>
          </div>
          <div class="nav-link">
            <a href="#case">
              Кейсы
            </a>
          </div>
          <div class="nav-link">
            <a href="#work">
              Принципы
            </a>
          </div>
          <div class="nav-link">
            <a href="#price">
              Услуги
            </a>
          </div>
          <div class="nav-link">
            <a href="#contacts">
              Контакты
            </a>
          </div>
        </div>
        <a>
          <div class="btn-send w-100 text-black">
            Оставить заявку
          </div>
        </a>
      </div>
    </div>
    <div class="d-lg-none">
      <b-navbar toggleable="lg" type="dark" variant="transparent">
        <b-navbar-brand href="/">
          <img src="../assets/img/logo.svg">
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse">
          <img class="open-block" src="../assets/img/navbutton.svg">
          <img class="close-block" src="../assets/img/close.svg">
        </b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="/">Главная</b-nav-item>
            <b-nav-item href="#case">Кейсы</b-nav-item>
            <b-nav-item href="#work">Принципы</b-nav-item>
            <b-nav-item href="#price">Услуги</b-nav-item>
            <b-nav-item href="#contacts">Контакты</b-nav-item>
            <div class="btn-send w-100 text-black">
              Оставить заявку
            </div>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavHeader'
}
</script>

<style scoped>

  .nav-link a {
    color: #fff!important;
  }

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

  .collapse {
    margin-left: -20px;
    margin-right: -20px;
    padding-left: 22px;
    margin-top: 10px;
    padding-top: 10px;
    border-top: 0.5px solid #fff;
  }

  .navbar {
    border-bottom: 0.5px solid #fff;
    margin-left: -20px;
    padding-left: 22px;
    margin-right: -20px;
  }

  .nav-link {
    align-self: center;
    cursor: pointer;
  }

  .navbar-dark .navbar-toggler {
    border: 0!important;
  }

  .not-collapsed .open-block {
    display: none;
  }

  .close-block {
    display: none;
  }

  .not-collapsed .close-block {
    display: block!important;
  }
  a {

  }

  .nav-link {
    color: #fff;
  }

  .not-collapsed > .navbar {
    background-color: white;
  }

  @media (max-width: 768px) {
    .navbar-brand, .navbar-toggler {
      z-index: 999;
    }

    .navbar-collapse {
      margin-top: -49px;
      background: #1F1F1F;
      padding-top: 66px;
    }

    .btn-send {
      margin-left: -19px;
      margin-right: -20px;
      width: 100%;
      max-width: 390px;
      padding: 10px 0;
      text-align: center;
      position: absolute;
      bottom: -40px;
    }
  }
</style>
