<template>
  <div class="noFound">
    <img
      src="../../assets/img/undraw_page_not_found_su7k.svg"
      alt="404"
      class="undraw"
    />
    <h1>sorry, page not found...</h1>
  </div>
</template>

<script>
export default {
  name: "notFound"
};
</script>

<style lang="scss" scoped>
.noFound {
  display: none;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100vh;
  background: #ffffff;
  border-bottom: 1px solid #f2f3f5;
  .undraw {
    width: 400px;
    height: 400px;
  }
}
@media only screen and (max-width: 600px) {
  .noFound {
    .undraw {
      width: 200px;
      height: 200px;
    }
  }
}
</style>
