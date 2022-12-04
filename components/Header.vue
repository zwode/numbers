<template>
  <div class="header-bg text-white">
    <ul class="circles">
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
    <div class="container index-position">
      <NavHeader />
    </div>
    <div class="main-header container index-position">
      <div>
        <div class="text-left main-text">
<!--          <strong>Бизнес меняет</strong><br>-->
<!--          <div class="content">-->
<!--            <div class="content__container">-->
<!--              <ul class="content__container__list">-->
<!--                <li class="content__container__list__item">стратегия</li>-->
<!--                <li class="content__container__list__item">команда</li>-->
<!--                <li class="content__container__list__item">подход</li>-->
<!--                <li class="content__container__list__item">принципы</li>-->
<!--                <li class="content__container__list__item">мышление</li>-->
<!--              </ul>-->
<!--            </div>-->
<!--          </div>-->
          <div>
            Превращаем<br>
            трафик из интернета<br>
            в ваших клиентов<br>
            <div class="un-header">
              Команда экспертов в digital маркетинге и интернет трафике в одном флаконе
            </div>
            <div class="d-flex">
              <div class="icon-header">
                <img src="../assets/img/inst.svg" alt="inst">
              </div>
              <div class="icon-header">
                <img src="../assets/img/facebook.png" alt="facebook">
              </div>
              <div class="icon-header">
                <img src="../assets/img/google.png" alt="google">
              </div>
              <div class="icon-header">
                <img src="../assets/img/yandex.png" alt="yandex">
              </div>
              <div class="icon-header">
                <img src="../assets/img/youtube.png" alt="youtube">
              </div>
              <div class="icon-header">
                <img src="../assets/img/vk.png" alt="vk">
              </div>
              <div class="icon-header">
                <img src="../assets/img/mytarget.png" alt="mytarget">
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import NavHeader from "./NavHeader";
export default {
  name: 'Header',
  components: { NavHeader }
}

</script>

<style scoped lang="scss">

.circles{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 730px;
  overflow: hidden;
}

.circles li{
  filter: blur(195.5px);
  opacity: 0.1;
  position: absolute;
  display: block;
  list-style: none;
  width: 20px;
  height: 20px;
  background: #542EEB;;
  animation: animate 25s linear infinite;
  bottom: 0px;

}

.circles li:nth-child(1){
  left: 25%;
  width: 80px;
  height: 80px;
  animation-delay: 12s;
}


.circles li:nth-child(2){
  left: 10%;
  width: 50px;
  height: 50px;
  animation-delay: 12s;
  animation-duration: 12s;
}

.circles li:nth-child(3){
  left: 70%;
  width: 50px;
  height: 50px;
  animation-delay: 14s;
}

.circles li:nth-child(4){
  left: 40%;
  width: 60px;
  background: #7058D0;
  height: 60px;
  animation-delay: 10s;
  animation-duration: 18s;
}

.circles li:nth-child(5){
  left: 65%;
  width: 50px;
  height: 50px;
  animation-delay: 10s;
}

.circles li:nth-child(6){
  left: 75%;
  width: 110px;
  background: #7058D0;
  height: 110px;
  animation-delay: 12s;
}

.circles li:nth-child(7){
  left: 35%;
  width: 150px;
  height: 150px;
  background: #542EEB;;
  animation-delay: 12s;
}

.circles li:nth-child(8){
  left: 50%;
  width: 50px;
  height: 50px;
  background: #542EEB;
  animation-delay: 12s;
  animation-duration: 12s;
}

.circles li:nth-child(9){
  left: 20%;
  width: 150px;
  height: 350px;
  animation-delay: 12s;
  animation-duration: 12s;
}

.circles li:nth-child(10){
  left: 85%;
  width: 150px;
  height: 150px;
  animation-delay: 0s;
  animation-duration: 5s;
}



@keyframes animate {

  0%{
    transform: translateY(0);
    opacity: 1;
    border-radius: 0;
  }

  25% {
    transform: translateY(-250px) translateX(random(400) + px);
    opacity: 1;
  }

  50% {
    transform: translateY(-500px) translateX(random(100) + px);
    opacity: 1;
  }

  75% {
    transform: translateY(-750px) translateX(random(3000) + px);
    opacity: 1;
  }

  100%{
    transform: translateY(0) translateX(random(1000) + px);
    opacity: 0;
    border-radius: 50%;
  }

}

.icon-header {
  margin-right: 20px;
}

.icon-header img {
  max-width: 65px;
  max-height: 65px;
}

.container {
  padding-top: 20px;
}

.un-header {
  font-size: 20px;
}

.main-header {
  padding-top: 30px;
  padding-bottom: 100px;
}

.traffic {
  margin-top: 105px;
  height: 100px;
  color: #fff!important;
  font-weight: 400;
  font-size: 24px;
  line-height: 34px;
  align-self: center;
}

.main-text {
  font-size: 96px;
  line-height: 98px;
}

@media (max-width: 768px) {

  .main-text {
    font-size: 33px;
    line-height: 34px;
  }
  .main-header {
    padding: 60px 20px;
    padding-bottom: 40px;
  }
  .header-bg {
    height: 313px;
  }
  .traffic {
    margin-top: 65px;
    font-size: 18px;
  }
}

.content {
  position: absolute;
  left: 50.38%;
  margin-top: 45px;
  transform: translate(-50%, -50%);
  overflow:hidden;

  font-family: 'Lato', sans-serif;
  font-size: 58px;
  line-height: 65px;
  color: #ecf0f1;

  &__container {
    font-weight: 600;
    overflow: hidden;
    height: 65px;
    padding: 0 40px;

    &__text {
      display: inline;
      float: left;
      margin: 0;
    }

    &__list {
      font-weight: normal;
      margin-top: 0;
      padding-left: 0;
      text-align: center;
      list-style: none;

      -webkit-animation-name: change;
      -webkit-animation-duration: 10s;
      -webkit-animation-iteration-count: infinite;
      animation-name: change;
      animation-duration: 10s;
      animation-iteration-count: infinite;

      &__item {
        line-height: 65px;
        margin: 0;
      }
    }
  }
}


@media (max-width: 768px) {
  .content {
    margin-top: 30px;
    font-size: 31px;

    &__container {
      height: 35px;
      &__list {
        &__item {
          line-height: 35px;
          margin: 0;
        }
      }
    }
  }
}

@-webkit-keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@-webkit-keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-20%,0);}
  33.32%,45.98% {transform:translate3d(0,-40%,0);}
  49.98%,62.64% {transform:translate3d(0,-60%,0);}
  66.64%,79.3% {transform:translate3d(0,-80%,0);}
  83.3%,95.96% {transform:translate3d(0,0%,0);}
}

@-o-keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@-o-keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-20%,0);}
  33.32%,45.98% {transform:translate3d(0,-40%,0);}
  49.98%,62.64% {transform:translate3d(0,-60%,0);}
  66.64%,79.3% {transform:translate3d(0,-80%,0);}
  83.3%,95.96% {transform:translate3d(0,0%,0);}
}

@-moz-keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@-moz-keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-20%,0);}
  33.32%,45.98% {transform:translate3d(0,-40%,0);}
  49.98%,62.64% {transform:translate3d(0,-60%,0);}
  66.64%,79.3% {transform:translate3d(0,-80%,0);}
  83.3%,95.96% {transform:translate3d(0,0%,0);}
}

@keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-20%,0);}
  33.32%,45.98% {transform:translate3d(0,-40%,0);}
  49.98%,62.64% {transform:translate3d(0,-60%,0);}
  66.64%,79.3% {transform:translate3d(0,-80%,0);}
  83.3%,95.96% {transform:translate3d(0,0%,0);}
}

@media (max-width: 425px) {
  .circles {
    height: 313px;
  }
  .un-header {
    font-size: 8px;
    line-height: 16px!important;
  }
  .main-header {
    padding: 5px 20px;
  }
  .icon-header {
    margin-right: 5px;
  }

  .icon-header img {
    max-width: 15px;
    max-height: 15px;
  }
}

</style>
