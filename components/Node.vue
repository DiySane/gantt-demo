<template>
  <!-- <div
    class="node"
    :style="
      'grid-row: ' + row + '; grid-column: ' + start + '; background: ' + color
    "
  > -->
  <div class="node" :style="'grid-column: 1; background: ' + color + ';'">
    {{ name }}
  </div>
</template>

<style scoped>
.node {
  color: white;
  font-size: auto;
  padding: 0px;
  /* background: #b03532; */
  grid-row: 1;
  min-width: 100%;
  height: auto;
  width: 100%;
  justify-self: center;
}
</style>

<script>
export default {
  props: {
    row: {
      type: Number
      //   default: 3
    },
    name: {
      type: String
      //   default: "empty"
    },
    start: {
      type: Number
      //   default: 3
    },
    color: {
      type: String
      //   default: "red"
    }
  },
  data() {
    return {};
  }
};
</script>
