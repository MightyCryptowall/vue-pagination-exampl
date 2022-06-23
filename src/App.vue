<template>
  <div class="container">
  <PaginationComponent
    :totalPages="10"
    :perPage="10"
    :currentPage="currentPage"
    @pagechanged="onPageChange"
  />
  </div>
</template>

<script>
import PaginationComponent from "./components/PaginationComponent.vue";

export default {
  name: "App",
  components: {
    PaginationComponent,
  },
  data() {
    return {
      currentPage: 1,
    };
  },
  methods: {
    onPageChange(page) {
      console.log(page);
      this.currentPage = page;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.container{
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
