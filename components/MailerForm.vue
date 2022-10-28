<template>
  <div>
    <b-form ref="form" @submit="onSubmit" class="form-block">

      <b-form-group class="custom-input" id="input-group-2" label-for="input-2">
        <b-form-input
          id="input-2"
          name="user_name"
          placeholder="Имя"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-1"
        label-for="input-1"
      >
        <b-form-input
          id="input-1"
          name="user_email"
          type="email"
          placeholder="Почта"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-3"
        label-for="input-3"
      >
        <b-form-input
          id="input-3"
          name="user_phone"
          placeholder="Телефон"
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-3"
        label-for="input-3"
      >
        <b-form-select
          name="user_type"
          :options="options"
          placeholder="Услуги"
        ></b-form-select>
      </b-form-group>

      <b-button type="submit" variant="primary">Отправить</b-button>
    </b-form>
    <div class="status-form d-none">
      <h1>
        Заявка отправлена!
      </h1>
    </div>
  </div>
</template>

<script>
import emailjs from '@emailjs/browser'

export default {
  data() {
    return {
      show: true,
      selected: 'Не выбирал',
      options: [
        { value: 'Таргетированная реклама', text: 'Таргетированная реклама' },
        { value: 'Контекстная реклама', text: 'Контекстная реклама' },
        { value: 'Разработкачат-ботов', text: 'Разработкачат-ботов' },
        { value: 'Создание сайтов', text: 'Создание сайтов' },
        { value: 'Консультации', text: 'Консультации' },
        { value: 'Обсуждение проекта', text: 'Обсуждение проекта'}
      ]
    }
  },
  methods: {
    onSubmit(event) {
      emailjs.sendForm('zwode02', 'valp.agency', this.$refs.form, 'dTjDaRZ3OuZdZYHPX')
        .then((result) => {
          console.log('SUCCESS!', result);
        }, (error) => {
          console.log('FAILED...', error);
        });
      this.show = false
      document.querySelector('.form-block').classList.add('d-none')
      document.querySelector('.status-form').classList.remove('d-none')

    }
  }
}
</script>

<style scoped>

</style>
