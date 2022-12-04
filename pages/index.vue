<template>
  <div>
    <Header />
    <div class="bg-gradient pb-5">
      <Cases />
    </div>
    <div class="container">
      <HowWork />
      <HowMuch />
    </div>
    <Footer />
  </div>
</template>

<script>

import HowWork from "../components/HowWork";
import HowMuch from "../components/HowMuch";
import Footer from "../components/Footer";

export default {
  name: 'IndexPage',
  components: {Footer, HowMuch, HowWork}
}

</script>
