<template>
  <div class="gantt">
    <h2 class="service-item" style="grid-row: 1; grid-column: 2/4; ">DAYS</h2>
    <h3 class="service-item" style="grid-row: 2; grid-column: 2">Sun</h3>
    <h3 class="service-item" style="grid-row: 2; grid-column: 3">Mon</h3>
    <h3 class="service-item" style="grid-row: 3; grid-column: 1">row1</h3>
    <h3 class="service-item" style="grid-row: 4; grid-column: 1">row2</h3>
    <!-- <div class="service-item" style="grid-row: 3; grid-column: 2">
      row1-item1
    </div>
    <div class="service-item" style="grid-row: 3; grid-column: 3">
    </div>
    <div class="service-item" style="grid-row: 4; grid-column: 2">
      row2-item-1
    </div>
    <div
      class="service-item"
      style="grid-row: 4; grid-column: 3; display: grid; grid-template-columns: repeat(2, 1fr); grid-gap: 5px;"
    >
      <p
        class="item-1"
        :style="'grid-row:' + model + ';grid-column: 1/3; height: 100%'"
      >
        task-1
      </p>
      <p class="item-2" style="grid-row: 2; grid-column: 1/3; height: 100%">
        task-2
      </p>
    </div> -->
    <TaskManager @addNode="acceptNode" />
    <!-- <div
      class="service-item"
      style="grid-row: 4; grid-column: 3; display: grid; grid-template-columns: repeat(2, 1fr); grid-gap: 5px;"
    > -->
      <div
        v-for="node in nodes"
        :key="node.id"
        class="service-item"
        :style="
          'grid-row: ' +
            node.row +
            '; grid-column:' +
            node.start +
            '; display: grid; grid-template-columns: auto; grid-template-rows: repeat(5, 1fr); grid-gap: 5px;'
        "
      >
        <Node :name="node.name" :color="node.color" />
      </div>
    </div>
  <!-- </div> -->
</template>

<style scoped>
.gantt {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px 0px;
  width: 100%;
  max-width: 1150px;
  padding-top: 40px;
  padding-left: 10px;
  padding-right: 10px;
  margin: 0 auto;
  /* grid-template-rows: auto auto auto; */
  grid-template-rows: repeat(40, 1fr);
  /* max-height: 10px; */
  border: 20px solid #f2f4f7;
  border-radius: 5px;
  /* background-color: #B388FF; */
  background-color: #e9ebf0;
  row-gap: 10px;
  column-gap: 10px;
}

.service-item {
  padding: 5px;
  text-align: center;
  border-top: 1px solid #3e2723;
  border-bottom: 1px solid #3e2723;
  border-left: 1px solid #3e2723;
  border-right: 1px solid #3e2723;
  min-width: 20px;
  min-height: 30px;
  color: black;
}

.item-1 {
  color: white;
  font-size: auto;
  padding: 0px;
  background: #b03532;
  grid-row: 1;
  min-width: 100%;
  height: auto;
  width: 100%;
  justify-self: center;
}
.item-2 {
  color: white;
  font-size: auto;
  padding: 0px;
  background: #32b075;
  grid-row: 2;
  min-width: 100%;
  height: auto;
  width: 100%;
  justify-self: center;
}

/* h2 {
  border: 2px solid #ffa94d;
  border-radius: 5px;
  background-color: #ffd8a8;
  padding: 1em;
  color: #d9480f;
} */
/* nodes */
</style>
<script>
import TaskManager from "@/components/task-manager";
import Node from "@/components/Node";
export default {
  data: () => ({
    model: 1,
    items: [
      { id: 2, name: '<p class="item-1">hey</p>' },
      { id: 3, name: "Chrome : app" },
      { id: 4, name: "Webstorm : app" },
      { id: 28, name: "Basic layouts : mp4" },
      { id: 29, name: "Advanced techniques : mp4" },
      { id: 30, name: "All about app : dir" },
      { id: 31, name: "Intro : mov" },
      { id: 32, name: "Conference introduction : avi" }
    ],
    nodes: []
  }),
  methods: {
    acceptNode(node) {
      this.nodes.push(node);
    }
  }
};
</script>
