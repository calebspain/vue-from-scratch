<template>
  <div class="card">
    <div class="header">
      <h2>{{ item.title }}</h2>
      <button type="button" @click="toggle = !toggle">Details</button>
    </div>
    <p v-if="toggle">{{ item.description }}</p>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props: ["item"],
  data: function() {
    return {
      toggle: false
    };
  }
};
</script>

<style scoped>
.card {
  width: 360px;
  margin: 0px auto;
  padding: 30px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  border: 2px solid #cdcdcd;
}

.card:first-of-type {
  margin-top: 30px;
}

.card > .header > h2 {
  float: left;
}

.card > .header > button {
  float: right;
  padding: 10px 20px;
  color: #fff;
  background: #004488;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.card > .header:after {
  content: "";
  display: table;
  clear: both;
}

.card > p {
  padding-top: 30px;
  border-top: 1px solid #cdcdcd;
}
</style>