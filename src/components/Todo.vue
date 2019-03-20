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
            <v-list>
              <v-list-tile
                v-for="(item, index) in items" 
                v-bind:key="index"
                @click="updateItem(index)">
                <v-list-tile-action>
                  <v-checkbox v-model="item.completed">
                  </v-checkbox>
                </v-list-tile-action>
                <v-list-tile-title>
                  {{ item.title }}
                </v-list-tile-title>
              </v-list-tile>
            </v-list>
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
      items: [
        { 
          title: "Item 1",
          completed: true 
        }, 
        { 
          title: "Item 2",
          completed: false
        },
        { 
          title: "Item 3",
          completed: false
        }
      ]
    };
  },
  methods: {
    addItem: function() {
      console.log("Add Item", this.newItem);
      if (this.newItem) {
        let item = { text: this.newItem };
        this.items.push(item);
        this.newItem = "";
      }
    },
    updateItem: function(index) {
      console.log("Update Item", index);
    },
    removeItem: function(index) {
      console.log("Remove Item", index);
    }
  }
};
</script>

<style></style>
