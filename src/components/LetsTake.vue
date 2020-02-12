<template>
  <v-container class="letsTake">
    <div class="overlap-spacer"></div>
    <v-row>
      <v-col cols="7" class="d-flex align-center">
        <div class="mk-text-dark">
          <h2 class="display-2 pb-6">
            Praplėsk savo<br />
            <span class="cyan--text lighten-3">Verslo</span> klientų ratą
          </h2>
          <p class="pb-9">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate
            placeat enim ipsam, soluta, reprehenderit mollitia magni vel
            asperiores perspiciatis iusto minima consectetur doloribus at.
            Dicta, possimus dolores? Laborum aliquam veritatis harum. Sequi,
            corrupti adipisci pariatur quas voluptates commodi officia expedita
            repellat accusantium iure, perferendis nihil blanditiis voluptatibus
            necessitatibus. Alias, quasi.
          </p>
          <v-btn class="mk-bg-grad-move px-8" rounded dark>Pradėk dabar</v-btn>
        </div>
      </v-col>
      <v-col cols="5">
        <v-img :src="getImgUrl('mk-coffe.png')"></v-img>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// import { eventBus } from "@/main.js";
export default {
  name: "LetsTake",
  data() {
    return {
      coffeImg: "@/assets/mk-coffe.png"
    };
  },
  methods: {
    getImgUrl(pic) {
      return require("../assets/" + pic);
    }
  }
};
</script>

<style lang="scss" scoped>
.letsTake {
  padding-bottom: 120px;
}
.overlap-spacer {
  height: 280px;
}
</style>
