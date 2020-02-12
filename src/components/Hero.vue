<template>
  <v-container fluid class="h-100 hero mk-overlay">
    <v-container
      class=" text-center h-100 flex-grow-1 d-flex align-center align-center"
    >
      <div class="w-100 white--text z-1">
        <h1 class="mk-main-heading white--text display-3 font-weight-bold">
          Labas,<br />
          <span class="font-weight-light"> ar norėtum </span> <br />
          savo svetainės?
        </h1>
        <small
          >Prisitaikančio dizaino, greitai veikiančios svetainės už protingą
          kainą</small
        >
      </div>
    </v-container>
    <v-container>
      <v-row class="three-blocks-row no-gutters z-1 d-flex justify-center">
        <v-col cols="4">
          <div class="hero-text-block text-center bg-accent white--text">
            <v-icon dark>mdi-access-point-network</v-icon>
            <h4 class="title">Pirminis SEO</h4>
            <p class="body-2">
              Priminis vidinis SEO leis google lengviau jus rasti
            </p>
          </div>
        </v-col>

        <v-col cols="4">
          <div
            class="hero-text-block hero-text-block--special mk-bg-grad-move text-center white--text"
          >
            <v-icon dark>mdi-laptop</v-icon>
            <h4 class="title">Pritakyta Visiems įrenginiams</h4>
            <p class="body-2">
              Priminis vidinis SEO leis google lengviau jus rasti
            </p>
          </div>
        </v-col>

        <v-col cols="4">
          <div class="hero-text-block text-center bg-accent white--text">
            <v-icon dark>mdi-facebook</v-icon>
            <h4 class="title">Facebook, Instagram integracija</h4>
            <p class="body-2">
              Priminis vidinis SEO leis google lengviau jus rasti
            </p>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: "Hero",
  data: () => ({})
};
</script>

<style lang="scss" scoped>
.hero {
  height: 100vh;
  background: url("../assets/mes-as-min.jpg") no-repeat center center;
  background-size: cover;
}
.z-1 {
  z-index: 1;
  position: relative;
}
.bg-accent {
  background-color: #26313c;
}

.hero-text-block {
  padding: 54px 24px 63px;
  .v-icon {
    margin-bottom: 34px;
    display: block;
    font-size: 40px;
  }
  h4 {
    font-size: 18px;
  }
  transition: scale 0.3s ease-in background-position 0.3s ease-in;
  &:hover .v-icon {
    transform: scale(1.2);
  }
}
.hero-text-block--special {
  padding: 79px 24px 88px;
  margin-top: -25px;
}
.three-blocks-row {
  // margin-top: -50px;
  transform: translateY(-35%);
}
</style>
