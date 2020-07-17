<template>
  <div class="gaskir-page">
    <section class="title">
      <h1>Tambah Petugas Parkir</h1>
    </section>
    <section class="main-menu">
      <aside class="list-gas"></aside>
      <div class="add-gas"></div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Gaskir"
};
</script>

<style lang="scss" scoped>
.gaskir-page {
  display: none;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .main-menu {
    display: flex;
    width: 100%;
    margin-bottom: 50px;
    padding: 30px;
    box-sizing: border-box;
    .list-gas {
      width: 30%;
      height: 900px;
      background: white;
      border-radius: 10px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
    }
    .add-gas {
      width: 70%;
      height: 900px;
      background: white;
      margin-left: 30px;
      border-radius: 10px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
    }
  }
}
</style>
