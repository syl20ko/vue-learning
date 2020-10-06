<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-md-12">
        <div class="jumbotron text-center h2">Contact Friends List</div>
        <contacts-list v-for="friend in friends" :key="friend.id"
        :name="friend.name"
        :adress="friend.adress"
        :telephoneNumber="friend.telephoneNumber"></contacts-list>
      </div>
    </div>
  </div>
</template>

<script>
import ContactsList from "./components/ContactsList.vue";

export default {
  name: "App",
  components: {
    ContactsList,
  },
  data() {
    return {
      friends: [
        {
          name: "Elie",
          adress: "Nice",
          telephoneNumber: "07 81 67 22 22",
        },
        {
          name: "Axel",
          adress: "Grasse",
          telephoneNumber: "06 81 67 33 33",
        },
      ],
    };
  },
};
</script>

<style>
</style>
