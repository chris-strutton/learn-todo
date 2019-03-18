<template>
  <v-container fluid fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md6>
        <v-card class="elevation-12">
          <v-toolbar dark color="indigo">
            <v-toolbar-title>The List</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-text-field
              placeholder="New item"
              v-model="newItem"
              v-on:keyup.enter="addItem"
            ></v-text-field>
            <v-btn icon large @click="addItem">
              <v-icon large>mdi-plus</v-icon>
            </v-btn>
          </v-toolbar>
          <v-card-text>
            <ul>
              <li v-for="(item, index) in items" v-bind:key="index">
                {{ index }} - {{ item.text }}
              </li>
            </ul>
            <p>{{ newItem }}</p>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: function() {
    return {
      newItem: "",
      items: [{ text: "item 1" }, { text: "item 2" }, { text: "item 3" }]
    };
  },
  methods: {
    addItem: function() {
      if (this.newItem) {
        let item = { text: this.newItem };
        this.items.push(item);
        this.newItem = "";
      }
    }
  }
};
</script>

<style></style>
