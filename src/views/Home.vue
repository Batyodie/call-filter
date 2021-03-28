<template>
  <div class="home md:container mx-auto p-5">
    <div class="flex justify-center">
      <h1 class="text-4xl">Рассчитать дешевый маршрут</h1>
    </div>
    <div class="grid grid-cols-2 gap-5 ">
      <SearchForm />
      <md-list style="background-color: initial;">
        <md-list-item>
          <ResultRoad />
        </md-list-item>
        <md-list-item>
          <ResultRoad />
        </md-list-item>
        <md-list-item>
          <ResultRoad />
        </md-list-item>
        <md-list-item>
          <ResultRoad />
        </md-list-item>
        <Paginate
          class="mt-8"
          :page-count="5"
          :page-range="3"
          :margin-pages="2"
          :click-handler="clickCallback"
          :container-class="'pagination'"
          :page-class="'page-item'"
        ></Paginate>
      </md-list>
    </div>
  </div>
</template>

<script>
import Paginate from "vuejs-paginate";

import ResultRoad from "../components/resultRoad/resultRoad.vue";
import SearchForm from "../components/searchForm/searchForm.vue";
export default {
  name: "Home",
  components: { SearchForm, ResultRoad, Paginate },
  methods: {
    clickCallback(pageNum) {
      console.log(pageNum);
    },
  },
};
</script>
<style scoped>
.pagination {
  display: flex;
  max-width: 80%;
  width: 100%;
  justify-content: space-around;
}
</style>
