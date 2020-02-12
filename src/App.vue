<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" absolute right temporary>
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <Navbar />

    <v-content>
      <Hero />
      <LetsTake />
    </v-content>
  </v-app>
</template>

<script>
import { eventBus } from "@/main.js";
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import LetsTake from "./components/LetsTake";

export default {
  name: "App",
  components: {
    Navbar,
    Hero,
    LetsTake
  },

  data: () => ({
    //
    drawer: null,
    items: [
      { title: "Home", icon: "mdi-dashboard" },
      { title: "About", icon: "mdi-question_answer" }
    ]
  }),
  created() {
    eventBus.$on("drawerClicked", () => {
      this.drawer = !this.drawer;
    });
  }
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

.mk-text-dark {
  color: #384141;
}

a {
  text-decoration: none;
}
.mk-bg-grad-move {
  background-image: linear-gradient(
    to right,
    #5192e1 0%,
    #23ced5 51%,
    #5192e1 100%
  );
  transition: background-position 0.3s ease-in;
  background-size: 200% auto;
  &:hover {
    background-position: right center;
  }
}

.w-100 {
  width: 100%;
}
.h-100 {
  height: 100%;
}
.mk-overlay {
  position: relative;
  &::after {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.4);
  }
}
</style>
