<template>
  <v-toolbar dark flat absolute class="w-100 transparent">
    <div class="d-flex align-center">
      <v-toolbar-title>WebsitesMK</v-toolbar-title>
    </div>

    <v-spacer></v-spacer>

    <a href="#" class="px-3 py-4 white--text">Pagrindinis</a>
    <a href="#" class="px-3 py-4 white--text">Apie</a>
    <a href="#" class="px-3 py-4 white--text">Atlikti darbai</a>

    <v-icon @click="drawerClicked()">mdi-menu</v-icon>
  </v-toolbar>
</template>

<script>
import { eventBus } from "@/main.js";
export default {
  name: "Navbar",
  data() {
    return {
      drawer: false
    };
  },
  methods: {
    drawerClicked() {
      eventBus.$emit("drawerClicked");
      this.drawer = !this.drawer;
    }
  }
};
</script>
