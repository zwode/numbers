<template>
  <div class="block-std">
    <div class="block-title">
      Принципы работы
    </div>
    <div class="d-flex justify-content-between flex-wrap">
      <div class="card d-flex">
        <div class="card-body">
          <img src="../assets/img/worktogether.svg" alt="" width="45px" height="45px" class="card-icon">
          <div class="card-title">
            Совместная<br>
            работа
          </div>
        </div>
        <div class="card-open">
          <div class="wrap"><span class="arrow--l-r" :class="{ 'right': !isActive, 'left': isActive }" @click="isActive = !isActive"><span></span><span></span><span></span><span></span><span></span></span></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HowWork',
  data() {
    return {
      isActive: false
    }
  },
  methods: {

  }
}
</script>

<style scoped>
.card {
  max-width: 540px;
  width: 100%;
  margin-right: 30px;
  flex-direction: row;
}

.card-body {
  padding: 25px 40px;
}

.card-open {
  border-left: 0.5px solid rgba(0, 0, 0, 0.125);
  height: 100%;
  padding: 25px 0;
  align-self: center;
}

.card-icon {
  margin-bottom: 40px;
}
</style>
