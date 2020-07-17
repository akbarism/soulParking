<template>
  <aside>
    <nav>
      <img src="../assets/img/logo.png" alt="logo" />
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
    <section class="sub-menu-a" @click="report">
      <div class="list-menu-a change-a">
        <div class="for-icon"><i class="fas fa-file-invoice"></i></div>
        Pelaporan
      </div>
      <div class="rot ate">
        <i class="fas fa-caret-down"></i>
      </div>
    </section>
    <ul class="list-a hide">
      <li><p>Laporan Trafik</p></li>
      <li><p>Laporan Pendapatan</p></li>
      <li><p>Pengaduan</p></li>
      <li><p>Laporan Member</p></li>
      <li><p>Laporan Gaskir</p></li>
      <li><p>Laporan Aplikasi</p></li>
    </ul>
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
    <section class="sub-menu-c" @click="userAd">
      <div class="list-menu-c change-c">
        <div class="for-icon"><i class="fas fa-user"></i></div>
        Sistem Admin
      </div>
      <div class="roq qte">
        <i class="fas fa-caret-down"></i>
      </div>
    </section>
    <ul class="list-c hide-c">
      <li><p>Lokir</p></li>
      <li><p>Pengguna</p></li>
      <li><p>Hardware</p></li>
    </ul>
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
            src="../assets/img/logout.svg"
            alt="dashboard"
            height="15px"
            width="15px"
          />
        </div>
        Keluar
      </div>
    </section>
  </aside>
</template>

<script>
export default {
  name: "sideBar",
  data() {
    return {
      isActive: "",
      localis: "board"
    };
  },
  methods: {
    gaskir() {
      this.isActive = "gaskir";
      this.localis = "loc";
      document.querySelector(".container").style.display = "none";
      document.querySelector(".gaskir-page").style.display = "flex";
    },
    lokir() {
      this.isActive = "lokir";
      this.localis = "loc";
    },
    tarif() {
      this.isActive = "tarif";
      this.localis = "loc";
    },
    sift() {
      this.isActive = "sift";
      this.localis = "loc";
    },
    produk() {
      this.isActive = "produk";
      this.localis = "loc";
    },
    bleach() {
      this.isActive = "bleach";
      this.localis = "loc";
    },
    aktivasi() {
      this.isActive = "aktivasi";
      this.localis = "loc";
    },
    set() {
      this.isActive = "set";
      this.localis = "loc";
    },
    report() {
      document.querySelector(".list-a").classList.toggle("hide");
      document.querySelector(".rot").classList.toggle("ate");
    },
    setLoc() {
      document.querySelector(".list-b").classList.toggle("hide-b");
      document.querySelector(".ros").classList.toggle("ste");
    },
    userAd() {
      document.querySelector(".list-c").classList.toggle("hide-c");
      document.querySelector(".roq").classList.toggle("qte");
    },
    dashboard() {
      this.localis = "board";
      document.querySelector(".container").style.display = "flex";
      document.querySelector(".gaskir-page").style.display = "none";
    }
  }
};
</script>

<style lang="scss" scoped>
aside {
  width: 17%;
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
          //   fill: #e8933d;
        }
      }
    }
  }
  .sub-menu-a {
    display: flex;
    justify-content: space-between;
    background: #f2f3f5;
    padding: 10px 15px;
    cursor: pointer;
    .list-menu-a {
      color: #e8933d;
      display: flex;
      .for-icon {
        width: 25px;
      }
    }
    .rot {
      transform: rotate(180deg);
      transition: 0.5s;
    }
    .ate {
      transform: none;
    }
    .change-a {
      color: #000000;
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
  .sub-menu-c {
    display: flex;
    justify-content: space-between;
    background: #f2f3f5;
    cursor: pointer;
    padding: 10px 15px;
    .list-menu-c {
      display: flex;
      color: #e8933d;
      .for-icon {
        width: 25px;
      }
    }
    .roq {
      transform: rotate(180deg);
      transition: 0.5s;
    }
    .qte {
      transform: none;
    }
    .change-c {
      color: #000000;
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
  .list-a {
    position: relative;
    list-style: none;
    transition: 0.9s;
    li {
      background: #ffffff;
      padding: 5px;
      color: #bababa;
      font-size: 15px;
      p {
        padding-left: 35px;
      }
    }
    li:hover {
      background: #f3c249;
      color: white;
    }
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
      p {
        padding-left: 35px;
      }
    }
    li:hover {
      background: #f3c249;
      color: white;
    }
  }
  .list-c {
    list-style: none;
    transition: 1s;
    margin-bottom: 25px;
    li {
      background: #ffffff;
      padding: 5px;
      color: #bababa;
      font-size: 15px;
      transition: 0.5s;
      p {
        padding-left: 35px;
      }
    }
    li:hover {
      background: #f3c249;
      color: white;
    }
  }
  .hide {
    opacity: 0;
    overflow: hidden;
    height: 0;
    transition: 0.5s;
  }
  .hide-b {
    opacity: 0;
    overflow: hidden;
    height: 0;
  }
  .hide-c {
    opacity: 0;
    overflow: hidden;
    height: 0;
  }
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
</style>
