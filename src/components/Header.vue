<template>
  <header id="topest">
    <div class="logo">
      <img src="../components/icons/best-logo.webp" />
    </div>
    <nav class="nav-bar">
      <div class="opt">What's New</div>
      <div class="dropdowns1">Browse Cards 
        <div class="mega-dropdown">
          <div class="options">
            <div class="catagories">Categories
              <div class="opt-list-cont">
                <ul class="opt-list">
                  <li>0% Into APR</li>
                  <li>Secured</li>
                  <li>Student</li>
                  <li>Low APR</li>
                  <li>Gas Reward</li>
                  <li>Balance Transfer</li>
                  <li>Credit Union</li>
                  <li>Cash Back</li>
                  <li>Auto Reward</li>
                  <li>No Foreign Transfer Fee</li>
                  <li>Bussiness</li>
                  <li>Fintech</li>
                  <li>Travel</li>
                  <li>Airline</li>
                  <li>No Annual Fee</li>
                  <li>Crypto</li>
                  <li>Dining</li>
                  <li>Hotel</li>
                  <li>Debit & Prepaid</li>
                  <li>Retail</li>
                </ul>
              </div>
            </div>
            <div class="card-issuers">Cards Issuers
              <div class="issues-cont">
                <ul class="issues-list">
                  <li>American Express</li>
                  <li>Barclay</li>
                  <li>Chase</li>
                  <li>U.S. Bank</li>
                  <li>Discover</li>
                  <li>Bank of America</li>
                  <li>Capital One</li>
                  <li>Citibank</li>
                  <li>Wells Fargo</li>
                  <li>View All</li>
                </ul>
              </div>
            </div>
            <div class="credits">Card Credits</div>
          </div>
        </div>
      </div>
      <div class="dropdowns2">Resources</div>
      <div class="dropdowns3">News & Articles</div>
      <div class="dropdowns4">Become a member</div>
    </nav>

    <div class="burger-menu">
      <div class="burger">
        <img src="../components/icons/menu.png" alt="burger-menu"  @click="block()" ref="burger"/>
        <img src="../components/icons/cross.png" alt="cross-menu" style="display: none;" v-on:click="hidden()" ref="cross">
      </div>
      <div class="burger-header" ref="blockheader" v-on:click="block()" >
        <div class="list-cont">
          <ul class="burger-list">
            <li>What's New </li>
            <li>Browse Cards <img src="../components/icons/arrow-up.png" alt="arrow"></li>
            <li>Resources <img src="../components/icons/arrow-up.png" alt="arrow"></li>
            <li>News & Articles <img src="../components/icons/arrow-up.png" alt="arrow"></li>
            <li>Become a Member <img src="../components/icons/arrow-up.png" alt="arrow"></li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data(){
    return{
      isactiver:false
    }
  },
 methods: {
  block() {
    this.$refs.blockheader.style.display = 'block'
    this.$refs.burger.style.display = 'none'
    this.$refs.cross.style.display = 'block'
  },
  hidden() {
    this.$refs.blockheader.style.display = 'none'
    this.$refs.burger.style.display = 'block'
    this.$refs.cross.style.display = 'none'
  }
 }
  
};
</script>

<style lang="scss">
header {
  background-color: white;
  border-bottom: 1px solid #eee;
  height: auto;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
  overflow: visible; // Changed to visible for debugging
}

.logo img {
  margin-left: 10px;
  width: 160px;
  height: 42px;
}

.nav-bar {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-right: 14px;

  div {
    padding: 6px;
    margin: 18px;
    font-family: Arial, Helvetica, sans-serif;
    color: dodgerblue;

    &:hover {
      cursor: pointer;
      color: black;
    }
  }

  .dropdowns1 {
    &:hover .mega-dropdown {
      display: block;
      animation: fade-in 0.5s ease-in-out forwards;
    }

    .mega-dropdown {
      background-color: white;
      border: 1px solid blue;
      display: none;
      padding: 0;
      cursor: auto;
      position: absolute;
      height: 254px;
      width: 994px;
      transform: translateX(-50%);
      border-radius: 0 0 10px 10px;
      visibility: visible;
      transition: opacity 200ms ease-in, visibility 200ms ease-in;
    }

    .options {
      display: flex;
      border-bottom: 1px solid #eee;
      margin: 6px;

      div {
        height: 30px;
        border: 1px solid white;
        border-radius: 12px;
        padding: 6px;
        margin: 10px;
        width: 308px;
        background-color: white;

        &:hover {
          box-shadow: 0 0 5px black;
        }
      }

      .catagories {
        position: relative;

        .opt-list-cont {
          height: 0;
          width: 0;
          padding: 0;
          margin: 0;
          border-radius: 0;
          transition: opacity 0.3s ease-in-out;
        }

        .opt-list {
          padding: 4px;
          position: absolute;
          top: 72px;
          width: 70vw;
          list-style: none;
          color: black;
          display: grid;
          grid-template-rows: repeat(5, 1fr);
          grid-template-columns: repeat(4, 1fr);
          line-height: 30px;

          li {
            display: inline;
            color: black;

            &:hover {
              color: blue;
            }
          }
        }
      }

      .card-issuers {
        position: relative;

        .issues-cont {
          transform: translateY(-50%);
          height: 0;
          width: 0;
          padding: 0;
          margin: 0;
          border-radius: 0;
          transition: opacity 0.3s ease-in-out;
        }

        .issues-list {
          padding: 4px;
          position: absolute;
          top: 72px;
          width: 70vw;
          list-style: none;
          color: black;
          display: grid;
          grid-template-rows: repeat(2, 4fr);
          grid-template-columns: repeat(4, 4fr);
          line-height: 30px;
        }

        &:hover .catagories {
          display: none;
        }
      }
    }
  }
}

.burger-menu {
  display: none;
  position: relative;
  z-index: 999; // Ensure this is high enough

  .burger {
    img {
      margin: 8px;

      &:hover {
        cursor: pointer;
      }
    }
  }

  .burger-header {
    box-shadow: 0 8px 12px rgb(48, 46, 46);
    position: absolute;
    transform: translate(-89.5%);
    top: 60px;
    padding: 10px;
    height: 220px;
    border-radius: 0 0 14px 14px;
    width: 450px;
    background-color: #fff;
    z-index: 1000; // Set this higher than .burger-menu
    display: none; // Initially hidden

    // You can add styles for when the burger is active here
    .list-cont{
     margin: 12px;
      .burger-list{
        list-style-type: none;
        display: flex;
        font-family: Roboto;
        font-size: 13px;
        color: #1b0db9e3;
        flex-direction: column;
        gap: 18px;

        li{
          display: flex;
          align-items: center;
          justify-content: space-between;

          img{
            transform: rotate(90deg);
          }
        }
      }
    }
  }
}

@keyframes fade-in {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media screen and (max-width: 450px) {
  .nav-bar {
    display: none;
  }
  .burger-menu {
    display: block;

  }
}
</style>
