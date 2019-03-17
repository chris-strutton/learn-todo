<template>
  <v-app>
    <v-toolbar app color="indigo" dark>
      <v-toolbar-title class="headline text-uppercase">
        Todo App
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat>
        <span class="mr-2">Register/Login</span>
        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content>
      <todo-component> </todo-component>
    </v-content>
  </v-app>
</template>

<script>
import Todo from "./components/Todo";

export default {
  name: "App",
  components: {
    "todo-component": Todo
  },
  data() {
    return {
      //
    };
  }
};
</script>
