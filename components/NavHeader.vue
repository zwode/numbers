<template>
  <div>
    <div>
      <div class="d-flex justify-content-between w-100 nav-container">
        <div></div>
        <div class="d-flex justify-content-center px-5 border-left-header">
          <div class="align-self-center">
            <img src="../assets/img/valp.svg">
          </div>
        </div>
        <b-dropdown no-caret class="custom-dropdown" right>
          <template #button-content>
            <svg data-v-ef294276="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="list" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-list b-icon bi"><g data-v-ef294276="" transform="translate(8 8) scale(2 2) translate(-8 -8)"><path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"></path></g></svg>
          </template>
          <div class="text-black nav-text text-center">
            <div class="nav-link">
              <a href="/">
                Главная
              </a>
            </div>
            <div class="nav-border"></div>
            <div class="nav-link">
              <a href="#case">
                Кейсы
              </a>
            </div>
            <div class="nav-border"></div>
            <div class="nav-link">
              <a href="#work">
                Принципы
              </a>
            </div>
            <div class="nav-border"></div>
            <div class="nav-link">
              <a href="#price">
                Услуги
              </a>
            </div>
            <div class="nav-border"></div>
            <div class="nav-link">
              <a href="#contacts">
                Контакты
              </a>
            </div>
          </div>
        </b-dropdown>
      </div>
    </div>
<!--    <div class="d-lg-none">-->
<!--      <b-navbar toggleable="lg" type="dark" variant="transparent">-->
<!--        <b-navbar-brand href="/">-->
<!--          <img src="../assets/img/valp.svg">-->
<!--        </b-navbar-brand>-->
<!--        <b-navbar-toggle target="nav-collapse">-->
<!--          <img class="open-block" src="../assets/img/navbutton.svg">-->
<!--          <img class="close-block" src="../assets/img/close.svg">-->
<!--        </b-navbar-toggle>-->

<!--        <b-collapse id="nav-collapse" is-nav>-->
<!--          <b-navbar-nav>-->
<!--            <b-nav-item href="/">Главная</b-nav-item>-->
<!--            <b-nav-item href="#case">Кейсы</b-nav-item>-->
<!--            <b-nav-item href="#work">Принципы</b-nav-item>-->
<!--            <b-nav-item href="#price">Услуги</b-nav-item>-->
<!--            <b-nav-item href="#contacts">Контакты</b-nav-item>-->
<!--            <b-button v-b-modal.form-send class="btn-send w-100 text-black cursor-pointer">-->
<!--              Оставить заявку-->
<!--            </b-button>-->
<!--            <b-modal id="form-send" title="СВЯЗАТЬСЯ С НАМИ" hide-footer>-->
<!--              <p class="my-4">-->
<!--                <mailer-form />-->
<!--              </p>-->
<!--            </b-modal>-->
<!--          </b-navbar-nav>-->
<!--        </b-collapse>-->
<!--      </b-navbar>-->
<!--    </div>-->
  </div>
</template>

<script>
import MailerForm from "./MailerForm";
export default {
  name: 'NavHeader',
  components: {MailerForm}
}
</script>

<style lang="scss" scoped>
  .nav-link a {
    color: #000!important;
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

  .btn-send {
    border-radius: 0!important;
  }

  a {

  }

  .nav-link {
    color: #fff;
  }

  .nav-border {
    border: 1.5px solid #234D97;
    background: #234D97;
    border-radius: 20px;
    width: 70%;
    margin: 0 auto;
  }

  .not-collapsed > .navbar {
    background-color: white;
  }

  @media (max-width: 768px) {
    .navbar-brand, .navbar-toggler {
      z-index: 999;
    }

    .navbar-brand {
      padding-top: 0!important;
    }

    .navbar {
      padding-top: 0!important;
    }

    .navbar-collapse {
      margin-top: -49px;
      background: #1F1F1F;
      padding-top: 66px;
    }

    .btn-send {
      height: 60px;
      border-radius: 0;
      margin-left: -19px;
      margin-right: -20px;
      width: 100%;
      max-width: 390px;
      padding: 10px 0;
      text-align: center;
      position: absolute;
      bottom: -50px;
      border: 0;
      border-bottom: 1px solid black;
    }
  }
  @media (max-width: 425px) {
    img {
      width: 50px;
    }
  }
</style>
