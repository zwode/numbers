<template>
  <div class="header-bg text-white">
    <div class="container">
      <NavHeader />
    </div>
    <div class="main-header">
      <div>
        <div class="text-center main-text">
          <strong>Бизнес меняет</strong><br>
          стратегия
        </div>
      </div>
    </div>
    <div class="traffic align-self-bottom text-white text-center">
      Трафик агентство для вашего бизнеса
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

<style scoped>

.main-header {
  padding: 100px;
}

.traffic {
  height: 100px;
  color: #fff!important;
  font-weight: 400;
  font-size: 24px;
  line-height: 34px;
  align-self: center;
}

.main-text {
  font-size: 60px;
  line-height: 75px;
}
</style>
