<template>
  <div class="gantt">
    <span class="d-1"></span>
    <span class="d-2"></span>
    <span class="d-3"></span>
    <span class="d-4"></span>
    <span class="d-5"></span>
    <span class="d-6"></span>

    <h3 class="h-sun">sun
        <p class="item-1">hey</p>
    </h3>
    <h3 class="h-mon">mon
        
    </h3>
    <h3 class="h-tue">tue

    <p class="item-1">hey</p>
    </h3>
    <h3 class="h-wed">wed</h3>
    <h3 class="h-thu">thu</h3>
    <h3 class="h-fri">fri</h3>
    <h3 class="h-sat">sat</h3>
    <v-spacer />
    <!-- div v-for="item in items" :key="item.id">
      <p v-html="item.name"></p>
    </div> -->
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
  grid-template-rows: auto auto auto;
}
/* dividers */
span {
  border-left: 1px solid lightgrey;
  grid-row: 1 / span 40;
  /* grid-row: auto; */
}

span.d-1 {
  grid-column: 3;
}
span.d-2 {
  grid-column: 4;
}
span.d-3 {
  grid-column: 5;
}
span.d-4 {
  grid-column: 6;
}
span.d-5 {
  grid-column: 7;
}
span.d-6 {
  grid-column: 8;
}

/* days */
h3 {
  text-align: center;
  grid-row: 1;
}

h3.h-sun {
  grid-column: 2 / span 1;
}
h3.h-mon {
  grid-column: 3 / span 1;
}
h3.h-tue {
  grid-column: 4 / span 1;
}
h3.h-wed {
  grid-column: 5 / span 1;
}
h3.h-thu {
  grid-column: 6 / span 1;
}
h3.h-fri {
  grid-column: 7 / span 1;
}
h3.h-sat {
  grid-column: 8 / span 1;
}

p {
  text-align: center;
  grid-row: auto;
  display: grid;
}

p.item-1 {
  color: white;
  font-size: 20px;
  padding: 20px;
  background: #b03532;
  grid-row: 4;
  /* display: grid; */
}
/* nodes */
</style>
<script>
export default {
  data: () => ({
    items: [
      { id: 2, name: "<p class=\"item-1\">hey</p>" },
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
