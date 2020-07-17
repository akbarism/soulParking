<template>
  <div class="home">
    <sideBar />
    <div class="main-menu">
      <nav>
        <div class="left">
          <i class="fas fa-angle-left"></i>
          <p>Sembunyikan Menu</p>
        </div>
        <div class="right">
          <div class="reg">
            <select name="kota" id="kota" class="city">
              <option value="1">DKI Jakarta</option>
            </select>
            <div class="orange"><i class="fas fa-plus"></i></div>
          </div>
          <div class="profile">
            <div class="image">
              <img src="../assets/img/ISYANA-SARASVATI-1.jpg" alt="profile" />
            </div>
            <div class="info">
              <p>Isyana Sarasvati</p>
              <p class="position">Super Admin</p>
            </div>
          </div>
        </div>
      </nav>
      <Dashboard />
      <Gaskir />
      <Footer />
    </div>
  </div>
</template>

<script>
import sideBar from "../components/sidebar.vue";
import Dashboard from "../components/Dashboard.vue";
import Footer from "../components/Footer.vue";
import Gaskir from "../components/gaskir.vue";

export default {
  name: "Home",
  components: {
    sideBar,
    Dashboard,
    Gaskir,
    Footer
  }
};
</script>
<style lang="scss" scoped>
.home {
  display: flex;
  width: 100%;

  .main-menu {
    width: 83%;
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
      height: 70px;
      background: #4a4a4a;
      padding: 10px;
      box-sizing: border-box;
      .left {
        display: flex;
        color: #ffffff;
        margin-left: 15px;
        p {
          margin-left: 5px;
          margin-top: -2px;
        }
      }
      .right {
        display: flex;
        .reg {
          display: flex;
          align-items: center;
          margin-right: 50px;
          .city {
            height: 30px;
            width: 150px;
            border: 0.5px solid #bababa;
            border-radius: 5px 0 0 5px;
            color: #bababa;
          }
          .orange {
            display: flex;
            align-items: center;
            justify-content: center;
            background: #e8933d;
            height: 30px;
            width: 30px;
            color: #ffffff;
            border-radius: 0 10px 10px 0;
          }
        }
        .profile {
          display: flex;
          margin-right: 30px;
          .image {
            img {
              border-radius: 50%;
              height: 40px;
              width: 40px;
            }
          }
          .info {
            margin-left: 10px;
            color: #ffffff;
            .position {
              font-weight: 500;
              font-size: 12px;
              margin-top: 3px;
            }
          }
        }
      }
    }
  }
}
</style>
