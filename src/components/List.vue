<template>
  <div>
    <p>ITEM</p>
    <Dropdown @update:option="optionUpdate"></Dropdown>
  </div>
</template>

<script>
import Dropdown from "./Dropdown";

export default {
  name: "List",
  components: {
    Dropdown
  },
  methods: {
    optionUpdate: function(value) {
      alert(value);
    }
  }
};
</script>

<style scoped>
</style>