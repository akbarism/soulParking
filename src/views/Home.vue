<template>
  <div class="home">
    <sideBar v-bind:isBerger="isBerger" />
    <div class="main-menu full-width">
      <nav>
        <div class="left" @click="slide">
          <div v-if="isBerger == false">
            <div class="hide-menu">
              <i class="fas fa-angle-left"></i>
              <p>Sembunyikan Menu</p>
            </div>
            <i class="fas fa-bars sauce"></i>
          </div>
          <div v-else>
            <i class="fas fa-bars berger"></i>
          </div>
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
      <Dashboard v-bind:isStretch="isStretch" v-bind:isPuck="isPuck" />
      <Gaskir v-bind:stretced="stretced" v-bind:stretching="stretching" />
      <notFound />
      <Footer />
    </div>
  </div>
</template>

<script>
import sideBar from "../components/base_/sidebar.vue";
import Dashboard from "../components/base_/Dashboard";
import Footer from "../components/module_/Footer";
import Gaskir from "../components/base_/gaskir";
import notFound from "../components/base_/notFound.vue";

export default {
  name: "Home",
  components: {
    sideBar,
    Dashboard,
    Gaskir,
    notFound,
    Footer
  },
  data() {
    return {
      isStretch: false,
      isPuck: false,
      isBerger: false,
      stretching: false,
      stretced: false
    };
  },
  methods: {
    slide() {
      document.querySelector(".sidebar").classList.toggle("slider");
      document.querySelector(".main-menu").classList.toggle("full-width");
      this.isStretch = !this.isStretch;
      this.isBerger = !this.isBerger;
      this.isPuck = !this.isPuck;
      this.stretching = !this.stretching;
      this.stretced = !this.stretced;
    }
  }
};
</script>
<style lang="scss" scoped>
.home {
  position: relative;
  display: flex;
  width: 100%;
  .full-width {
    width: 83vw;
    margin-left: 230px;
  }
  .main-menu {
    width: 100%;
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
        cursor: pointer;
        .hide-menu {
          display: flex;
          p {
            margin-left: 5px;
            margin-top: -2px;
          }
        }
        .sauce {
          display: none;
        }
        .berger {
          font-size: 30px;
          color: #f3c249;
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
            background: #f3c249;
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
@media only screen and(max-width: 600px) {
  .home {
    .main-menu {
      width: 100%;
      nav {
        .left {
          margin-right: 10px;
          .hide-menu {
            display: none;
          }
          .sauce {
            display: block;
            font-size: 30px;
            color: #f3c249;
          }
        }
        .right {
          .reg {
            margin-right: 20px;
          }
          .profile {
            .info {
              display: none;
            }
          }
        }
      }
    }
    .full-width {
      width: 100%;
      margin-left: 0;
    }
  }
}
</style>
