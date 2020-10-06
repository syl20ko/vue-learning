<template>
  <div class="card mt-3">
    <div class="card-header">
      {{ name }}
      <span class="float-right"
        ><button @click="toggleInfo" class="btn btn-info">
          {{ buttonCaption }}
        </button></span
      >
    </div>
    <div v-if="visibleInfo">
      <div class="card-body">{{ adress }}</div>
      <div class="card-footer">{{ telephoneNumber }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactList",
  data() {
    return {
      visibleInfo: true,
    };
  },
  props: {
    name: {
      type: String,
      required: true,
    },
    adress: {
      type: String,
      required: true,
    },
    telephoneNumber: {
      type: String,
      required: true,
    },
  },
  computed: {
    buttonCaption() {
      return this.visibleInfo ? 'Hide List' : 'Show List';
    },
  },
  methods: {
    toggleInfo() {
      this.visibleInfo = !this.visibleInfo;
    },
  },
};
</script>

<style>
</style>