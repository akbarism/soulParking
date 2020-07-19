<template>
  <aside class="sidebar slider">
    <nav>
      <img src="../../assets/img/logo.png" alt="logo" />
      <h1>Management System</h1>
    </nav>
    <section class="dashboard" @click="dashboard">
      <div class="list-menu" v-bind:class="{ loca: localis == 'board' }">
        <div class="for-icon">
          <svg
            version="1.1"
            id="Capa_1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            viewBox="0 0 384 384"
            style="enable-background:new 0 0 384 384;"
            xml:space="preserve"
          >
            <g>
              <g>
                <g>
                  <rect x="213.333" y="0" width="170.667" height="128" />
                  <rect x="0" y="0" width="170.667" height="213.333" />
                  <rect x="0" y="256" width="170.667" height="128" />
                  <rect
                    x="213.333"
                    y="170.667"
                    width="170.667"
                    height="213.333"
                  />
                </g>
              </g>
            </g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
            <g></g>
          </svg>
        </div>
        Dashboard
      </div>
    </section>
    <Report />
    <section class="sub-menu-b" @click="setLoc">
      <div class="list-menu-b" v-bind:class="{ loca: localis == 'loc' }">
        <div class="for-icon"><i class="fas fa-cog"></i></div>
        Pengaturan Lokasi
      </div>
      <div class="ros ste">
        <i class="fas fa-caret-down"></i>
      </div>
    </section>
    <ul class="list-b hide-b">
      <li v-bind:class="{ active: isActive == 'lokir' }" @click="lokir">
        <p>Lokir</p>
      </li>
      <li v-bind:class="{ active: isActive == 'tarif' }" @click="tarif">
        <p>Tarif</p>
      </li>
      <li v-bind:class="{ active: isActive == 'gaskir' }" @click="gaskir">
        <p>Gaskir</p>
      </li>
      <li v-bind:class="{ active: isActive == 'sift' }" @click="sift">
        <p>Shift</p>
      </li>
      <li v-bind:class="{ active: isActive == 'produk' }" @click="produk">
        <p>Produk</p>
      </li>
      <li v-bind:class="{ active: isActive == 'bleach' }" @click="bleach">
        <p>Pemutihan kendaraan</p>
      </li>
      <li v-bind:class="{ active: isActive == 'aktivasi' }" @click="aktivasi">
        <p>Aktivasi Member</p>
      </li>
      <li v-bind:class="{ active: isActive == 'set' }" @click="set">
        <p>Pengaturan Pengguna</p>
      </li>
    </ul>
    <adminSystem />
    <section class="sub-menu-d">
      <div class="list-menu-d">
        <div class="for-icon"><i class="fas fa-user-circle"></i></div>
        Sistem Admin
      </div>
    </section>
    <section class="sub-menu-e">
      <div class="list-menu-e">
        <div class="for-icon">
          <img
            src="../../assets/img/logout.svg"
            alt="dashboard"
            height="15px"
            width="15px"
          />
        </div>
        Keluar
      </div>
    </section>
    <section class="hide-menu" @click="slide">
      <i class="fas fa-angle-left"></i>
      <p>Sembunyikan Menu</p>
    </section>
  </aside>
</template>

<script>
import Report from "../base_/report.vue";
import adminSystem from "../base_/adminSystem.vue";

export default {
  name: "sideBar",
  components: {
    Report,
    adminSystem
  },
  data() {
    return {
      isActive: "",
      localis: "board",
      isBerger: true
    };
  },
  methods: {
    slide() {
      document.querySelector(".sidebar").classList.toggle("slider");
      document.querySelector(".main-menu").classList.toggle("full-width");
      this.isBerger = !this.isBerger;
    },
    gaskir() {
      this.isActive = "gaskir";
      this.localis = "loc";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "flex";
      document.querySelector(".noFound").style.display = "none";
    },
    lokir() {
      this.isActive = "lokir";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    tarif() {
      this.isActive = "tarif";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    sift() {
      this.isActive = "sift";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    produk() {
      this.isActive = "produk";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    bleach() {
      this.isActive = "bleach";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    aktivasi() {
      this.isActive = "aktivasi";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    set() {
      this.isActive = "set";
      this.localis = "loc";
      document.querySelector(".noFound").style.display = "flex";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "none";
    },
    setLoc() {
      document.querySelector(".list-b").classList.toggle("hide-b");
      document.querySelector(".ros").classList.toggle("ste");
      // document.querySelector(".noFound").style.display = "flex";
    },
    dashboard() {
      this.localis = "board";
      this.isActive = "";
      document.querySelector(".container").style.display = "flex";
      document.querySelector(".gaskir-page").style.display = "none";
      document.querySelector(".noFound").style.display = "none";
    }
  }
};
</script>

<style lang="scss" scoped>
.sidebar {
  position: absolute;
  left: -230px;
  transition: 0.5s;
  width: 230px;
  height: 100%;
  background: white;
  box-shadow: 0px 3px 5px rgba(0, 0, 0, 0.25);
  z-index: 1;
  nav {
    height: 50px;
    background: #ffffff;
    padding: 10px;

    h1 {
      position: absolute;
      font-size: 16px;
      left: 40px;
      top: 30px;
      padding: 0;
      margin: 0;
    }
  }
  .dashboard {
    display: flex;
    justify-content: space-between;
    background: #f2f3f5;
    padding: 10px 15px;
    cursor: pointer;
    .list-menu {
      display: flex;
      .for-icon {
        width: 25px;
        svg {
          height: 13px;
          width: 15px;
        }
      }
    }
  }
  .sub-menu-b {
    display: flex;
    justify-content: space-between;
    background: #f2f3f5;
    padding: 10px 15px;
    cursor: pointer;
    .list-menu-b {
      display: flex;
      .for-icon {
        width: 25px;
      }
    }
    .ros {
      transform: rotate(180deg);
      transition: 0.5s;
    }
    .ste {
      transform: none;
    }
  }

  .sub-menu-d {
    display: flex;
    justify-content: space-between;
    background: #ffffff;
    padding: 0px 15px;
    .list-menu-d {
      padding-top: 25px;
      border-top: 1px solid #f2f3f5;
      cursor: pointer;
      display: flex;
      .for-icon {
        width: 25px;
      }
    }
  }
  .sub-menu-e {
    display: flex;
    justify-content: space-between;
    background: #ffffff;
    padding: 10px 15px;
    .list-menu-e {
      cursor: pointer;
      display: flex;
      .for-icon {
        width: 25px;
      }
    }
  }
  .hide-menu {
    display: none;
  }
  .list-b {
    list-style: none;
    transition: 0.5s;
    li {
      background: #ffffff;
      padding: 5px;
      color: #bababa;
      font-size: 15px;
      transition: 0.5s;
      cursor: pointer;

      p {
        padding-left: 35px;
      }
    }
    li:hover {
      background: #f3c249;
      color: white;
    }
  }

  .hide-b {
    opacity: 0;
    overflow: hidden;
    height: 0;
  }
}
.slider {
  left: 0;
  transition: 0.5s;
}
.active {
  background: #f3c249 !important;
  color: white !important;
}
.loca {
  color: #e8933d !important;
  svg {
    fill: #e8933d !important;
  }
}
@media only screen and (max-width: 600px) {
  .sidebar {
    width: 230px;
    .hide-menu {
      display: flex;
      padding: 15px;
      p {
        margin-left: 5px;
        margin-top: -2px;
      }
    }
  }
}
</style>
