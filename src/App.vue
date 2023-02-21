<script>
import MyTitle from './components/MyTitle.vue';
import NavBar from './components/NavBar.vue';
export default {
  components: { MyTitle, NavBar },
}
</script>

<template>
  <NavBar></NavBar>
  <div class="container">
    <section class="fullpage fullpage-1">
      <MyTitle>
        <template v-slot:title>Style & Beauty</template>
        <template v-slot:subtitle>New fashion brand</template>
      </MyTitle>
    </section>
    <section class="fullpage fullpage-2">
      <MyTitle>
        <template v-slot:title>Living Room Girls</template>
        <template v-slot:subtitle>Interior Design - Red Room</template>
      </MyTitle>
    </section>
    <section class="fullpage fullpage-3">
      <MyTitle>
        <template v-slot:title>The shape of water flowers</template>
        <template v-slot:subtitle>Book Cover</template>
      </MyTitle>
    </section>
    <section class="fullpage fullpage-4">
      <MyTitle>
        <template v-slot:title>Capturing the sunlight</template>
        <template v-slot:subtitle>Fashion Photoshoot</template>
      </MyTitle>
    </section>
    <section class="fullpage fullpage-5">
      <MyTitle>
        <template v-slot:title>Looking on the other side</template>
        <template v-slot:subtitle>Portrait photography</template>
      </MyTitle>
    </section>
  </div>
</template>

<style scoped>
.fullpage {
  height: 100vh;
  width: 100%;
}
.fullpage-1 {
  background: url('./assets/bg-1.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.fullpage-2 {
  background: url('./assets/bg-2.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.fullpage-3 {
  background: url('./assets/bg-3.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.fullpage-4 {
  background: url('./assets/bg-4.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.fullpage-5 {
  background: url('./assets/bg-5.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.container {
  max-height: 100vh;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
}
.fullpage {
  scroll-snap-align: start;
}
</style>
