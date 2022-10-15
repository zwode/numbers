<template>
  <div class="footer-bg" id="contacts">
    <div class="container footer d-flex justify-content-between text-white d-mob-block">
      <div class="footer-contact">
        <div class="title-contact">
          Telegram
        </div>
        <div class="link-contact">
          <a href="t.me/yourtg">
            t.me/yourtg
          </a>
        </div>
      </div>
      <div class="footer-contact">
        <div class="title-contact">
          WhatsApp
        </div>
        <div class="link-contact">
          <a href="web.whatsapp">
            web.whatsapp
          </a>
        </div>
      </div>
      <div class="footer-contact">
        <div class="title-contact">
          Телефон
        </div>
        <div class="link-contact">
          <a href="tel:+77002551996">
            +7 700 255 19 96
          </a>
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

.footer-contact {

}

.title-contact {
  color: #C3C3C3;
  font-size: 16px;
}

.link-contact a {
  font-size: 18px;
  color: #ffffff;
}

.title-contact {
  margin-bottom: 20px;
}

.footer {
  padding: 50px 0;
}

.footer-bg {
  background: linear-gradient(114.93deg, rgba(111, 81, 210, 0.35) 0%, rgba(0, 0, 0, 0) 66.44%), linear-gradient(258.39deg, #15185B -6.72%, #000000 100%);
}

@media (max-width: 768px) {
  .footer {
    padding: 15px;
    font-size: 20px;
  }
  .title-contact {
    margin-bottom: 0;
    font-size: 20px;
  }
  .link-contact {
    margin-bottom: 25px!important;
  }
  .link-contact a {
    font-size: 26px!important;
  }
}

</style>
