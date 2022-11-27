<template>
  <div class="footer-bg" id="contacts">
    <div class="container footer d-flex text-white">
      <div class="footer-main-text">
        Связаться<br>
        с нами
      </div>
      <div class="footer-link-text">
        <div class="footer-contact">
          <div class="link-contact">
            <a href="info@valp.agency">
              info@valp.agency
            </a>
          </div>
        </div>
        <div class="footer-contact">
          <div class="link-contact">
            <a href="https://t.me/valikhanp">
              Написать в Telegram
            </a>
          </div>
        </div>
        <div class="footer-contact">
          <div class="link-contact">
            <a href="https://api.whatsapp.com/send?phone=77002551996">
              Написать в Whatsapp
            </a>
          </div>
        </div>
        <div class="footer-contact">
          <div class="link-contact">
            <a href="tel:+77002551996">
              +7 700 255 19 96
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>

.footer-link-text {
  margin-left: 15%;
}

.footer-main-text {
  padding-right: 15%;
  border-right: 3px solid #fff!important;
  font-size: 48px;
}

.footer-contact {

}

.title-contact {
  color: #C3C3C3;
  font-size: 16px;
}

.link-contact a {
  font-size: 38px;
  color: #ffffff;
}

.title-contact {
  margin-bottom: 20px;
}

.footer {
  padding: 50px 0;
}

.footer-bg {
  background: #234D97;
}

@media (max-width: 768px) {
  .footer-main-text {
    padding-right: 15%;
    font-size: 18px;
    border-right: 1px solid #fff!important;
  }
  .footer-link-text {
    margin-left: 10%;
  }
  .link-contact a {
    font-size: 14px!important;
    color: #ffffff;
  }
  .footer {
    padding: 15px;
    font-size: 20px;
  }
  .title-contact {
    margin-bottom: 0;
    font-size: 20px;
  }
}

</style>
