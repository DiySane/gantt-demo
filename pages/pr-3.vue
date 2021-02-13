<template>
  <div class="gantt">
    <!-- <span class="d-left"></span> -->
    <span class="d-1"></span>
    <span class="d-2"></span>
    <span class="d-3"></span>

    <h3 class="h-left"></h3>
    <h3 class="h-sun">sun</h3>
    <h3 class="h-mon">
      mon
      <!-- <p class="item-1">hey</p> -->
    </h3>
    <div
      style="border-top: 1px solid #dfdfdf; border-bottom: 1px solid #dfdfdf; grid-row:2;"
    >
      <h2 style="grid-column: 1; text-align: center;">
        row-1
      </h2>
      <!-- <div style="grid-row: 10; border-bottom: 1px solid lightgrey;" /> -->

      <!-- <hr class="display: block; grid-row: 10; border: 10px solid green; border-radius: 5px;" > -->
      <div style="grid-column: 3; text-align: center;">
        <div
          style="display: inline-grid; grid-template-rows: repeat(2, 1fr); grid-template-columns: repeat(3, 1fr)"
        >
          <p class="item-1" style="grid-row: 1; grid-column: 3; height: 100%">
            task-1
          </p>
          <p class="item-2" style="grid-row: 2; grid-column: 1; height: 100%">
            task-2
          </p>
        </div>
      </div>
    </div>

    <h2 style="grid-column: 1 / 3; grid-row: 3; text-align: center;">
      row-2
    </h2>
    <!-- <hr style="grid-row: 20; border: 20px solid lightgrey;" /> -->
    <h3 class="h-drawer">template</h3>
  </div>
</template>

<style scoped>
.gantt {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-gap: 10px 0px;
  width: 100%;
  max-width: 1150px;
  padding-top: 40px;
  margin: 0 auto;
  /* grid-template-rows: auto auto auto; */
  grid-template-rows: repeat(40, 1fr);
  /* max-height: 10px; */
  border: 20px solid lightgrey;
  border-radius: 5px;
  background-color: #cf7c10;
  row-gap: 10px;
  -ms-grid-row-align: 3px black;
  column-rule-width: 100px;
}
/* dividers */
span {
  border-left: 1px solid lightgrey;
  grid-row: 1 / span 40;
  /* grid-template-rows: repeat(40, 1fr); */
  /* grid-row: auto; */
}

/* span.d-left {
  grid-column: 1;
} */
span.d-left {
  grid-column: 1 / 3;
}
span.d-1 {
  grid-column: 3 / 5;
}
span.d-2 {
  grid-column: 5 / 7;
}
span.d-3 {
  grid-column: 7 / 9;
}

/* days */
h3 {
  text-align: center;
  /* display: inline-grid; */
  grid-row: 1;
  /* grid-template-rows: repeat(40, 1fr); */
  /* grid-auto-flow: dense; */
  /* max-height: 30px; */
  row-gap: 1px;
}

h3.h-left {
  grid-column: 1 / 3;
}
h3.h-sun {
  grid-column: 3 / 5;
  /* grid-row: 1 / 1/2; */
  /* max-height: 12px; */
}
h3.h-mon {
  grid-column: 5 / 7;
}
h3.h-drawer {
  grid-column: 7 / 9;
}

/* p {
  text-align: center;
  grid-row: auto;
  display: grid;
} */

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
export default {
  data: () => ({
    items: [
      { id: 2, name: '<p class="item-1">hey</p>' },
      { id: 3, name: "Chrome : app" },
      { id: 4, name: "Webstorm : app" },
      { id: 28, name: "Basic layouts : mp4" },
      { id: 29, name: "Advanced techniques : mp4" },
      { id: 30, name: "All about app : dir" },
      { id: 31, name: "Intro : mov" },
      { id: 32, name: "Conference introduction : avi" }
    ]
  })
};
</script>
