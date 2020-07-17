<template>
  <div class="container">
    <div class="title">
      <h1>Dashboard</h1>
    </div>
    <section class="data-1">
      <div class="card-ppl">
        <div class="nomine">
          <section class="count">
            <h5>KEDATANGAN</h5>
            <H2 class="cn-1">2.500</H2>
          </section>
          <section class="icon">
            <img
              src="../assets/img/fds.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl">
        <div class="nomine">
          <section class="count">
            <h5>PJP LAMA</h5>
            <H2 class="cn-2">2.000</H2>
          </section>
          <section class="icon">
            <img
              src="../assets/img/refresh.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="grn"><b>+20%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl">
        <div class="nomine">
          <section class="count">
            <h5>PJP BARU</h5>
            <H2 class="cn-3">500</H2>
          </section>
          <section class="icon">
            <img
              src="../assets/img/plus.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="red"><b>-5%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-ppl">
        <div class="nomine">
          <section class="count">
            <h5>KELUAR</h5>
            <H2 class="cn-4">1.500</H2>
          </section>
          <section class="icon">
            <img
              src="../assets/img/exit.svg"
              alt="icon"
              height="100px"
              width="100px"
            />
          </section>
        </div>
        <div class="footer">
          <p class="red"><b>-15%</b> dari minggu lalu</p>
        </div>
      </div>
    </section>
    <section class="data-2">
      <div class="card-data">
        <h4>TOTAL PEMASUKAN</h4>
        <section class="income">
          <h1>RP. 1.500.000</h1>
          <p class="grn"><b>+30%</b> dari bulan lalu</p>
        </section>
        <section class="cart"></section>
        <div class="footer">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data">
        <h4>MEMBERSHIP</h4>
        <section class="income">
          <h1>1.200</h1>
          <p class="red"><b>-10%</b> dari bulan lalu</p>
        </section>
        <section class="cart"></section>
        <div class="footer">
          <p class="red"><b>-10%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data">
        <h4>METODE PEMBAYARAN</h4>
        <section class="cart"></section>
        <div class="footer-2">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
      <div class="card-data">
        <h4>TRAFIK SITUS</h4>
        <section class="cart"></section>
        <div class="footer-2">
          <p class="grn"><b>+30%</b> dari minggu lalu</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Dashboard"
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  width: 100%;
  background: #f2f3f5;
  .title {
    padding: 15px;
  }
  .data-1 {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    .card-ppl {
      width: 240px;
      height: 150px;
      background: #ffffff;
      border-radius: 10px;
      margin: 30px 0 0 30px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      box-sizing: border-box;
      overflow: hidden;
      .nomine {
        padding: 10px;
        display: flex;
        .count {
          width: 60%;
          h5 {
            margin-bottom: 15px;
          }
          .cn-1 {
            font-size: 30px;
            color: #82bf96;
          }
          .cn-2 {
            font-size: 30px;
            color: #924a9f;
          }
          .cn-3 {
            font-size: 30px;
            color: #5993dd;
          }
          .cn-4 {
            font-size: 30px;
            color: #d2353f;
          }
        }
      }
      .footer {
        height: 30px;
        width: 100%;
        background: #fcf3db;
        padding: 5px;
        .grn {
          font-size: 12px;
          color: #82bf96;
        }
        .red {
          font-size: 12px;
          color: #d2353f;
        }
      }
    }
  }
  .data-2 {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    margin-bottom: 50px;
    .card-data {
      padding: 10px;
      box-sizing: border-box;
      width: 510px;
      height: 300px;
      background: #ffffff;
      border-radius: 10px;
      margin: 30px 0 0 30px;
      box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.25);
      h4 {
        display: flex;
        width: 100%;
        margin-bottom: 30px;
      }
      .income {
        width: 100%;
        display: flex;
        justify-content: space-between;
        margin-bottom: 5px;
        .grn {
          font-size: 13px;
          color: #82bf96;
        }
        .red {
          font-size: 13px;
          color: #d2353f;
        }
      }
      .cart {
        width: 100%;
        height: 200px;
        background: #82bf96;
      }
      .footer {
        display: none;
        .grn {
          font-size: 12px;
          color: #82bf96;
        }
        .red {
          font-size: 12px;
          color: #d2353f;
        }
      }
      .footer-2 {
        display: none;
      }
    }
  }
}
@media only screen and (max-width: 600px) {
  .container {
    .data-1 {
      .card-ppl {
        .footer {
          display: flex;
          justify-content: center;
        }
      }
    }
    .data-2 {
      .card-data {
        width: 240px;
        height: 190px;
        padding: 10px 0 0 0;
        overflow: hidden;
        h4 {
          justify-content: center;
          margin-bottom: 0;
          font-size: 12px;
        }
        .income {
          h1 {
            margin: 0;
          }
          justify-content: center;
          .grn {
            display: none;
          }
          .red {
            display: none;
          }
        }
        .cart {
          height: 100px;
          margin-top: 10px;
        }
        .footer {
          display: flex;
          width: 100%;
          justify-content: center;
          margin-top: 5px;
        }
        .footer-2 {
          display: flex;
          align-items: center;
          background: #fcf3db;
          height: 30px;
          width: 100%;
          justify-content: center;
          margin-top: 25px;
          .grn {
            font-size: 13px;
            color: #82bf96;
          }
          .red {
            font-size: 13px;
            color: #d2353f;
          }
        }
      }
    }
  }
}
</style>
