<template>
  <div>
    <Header />
    <div class="container">
      <Cases />
      <HowWork />
    </div>
  </div>
</template>

<script>

import HowWork from "../components/HowWork";
export default {
  name: 'IndexPage',
  components: {HowWork}
}

</script>
