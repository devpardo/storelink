<template>

  <div class="nav-wrapper">
    <div v-if="menuShown" class="menu-content" :class="{'slideInDown animated': menuShown}">
      <div class="container">
        <div class="navigation pt-1 mb-5">
          <a href="#" class="logo"></a>

          <div class="menu">
            <a href="#" class="btn btn-primary btn-lg mr-1 uppercase small">THE VAULT</a>
            <a href="#" class="btn btn-lg btn-outline uppercase small mr-5">RIOT BRANDS</a>
            <a href="#" @click="showMenu" class="ml-5 menu-btn menu-close"></a>
          </div>
          
        </div>

        <div class="menu-items pb-1 mb-2">
          <a href="#" class="menu-item pb-1">The Storelink Difference</a>
          <a href="#" class="menu-item pb-1">Partners</a>
          <a href="#" class="menu-item pb-1">What We Do</a>
          <a href="#" class="menu-item pb-1">Retailers</a>
          <a href="#" class="menu-item pb-1">Building Brands</a>
          <a href="#" class="menu-item pb-1">New Business Enquiries</a>
          <a href="#" class="menu-item pb-1">Services</a>
        </div>

        <div class="sub-menu-items pb-1">
          <div class="sub-menu-group">
            <ul>
              <li class="mb-1">Our Team</li>
              <li class="mb-1">About Us</li>
              <li class="mb-1">Latest News</li>
            </ul>
          </div>
          <div class="sub-menu-group">
            <ul>
              <li class="mb-1">Careers</li>
              <li class="mb-1">Contact Us</li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="navigation  pt-1">
        <a href="#" class="logo"></a>

        <div class="menu">
          <a href="#" @click="showMenu" class="menu-btn"></a>
        </div>
        
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      menuShown: false
    }
  },
  methods: {
    showMenu(e) {
      e.preventDefault();
      //this.menuShown = !this.menuShown;

      var self = this;
      self.menuShown = !self.menuShown;
      //setTimeout(function(){ self.menuShown = false; }, 1000);

      if(this.menuShown) {
        document.body.classList.add('menu-open');
      } else {
        document.body.classList.remove('menu-open');
      }
    }
  }
}
</script>

<style scoped lang="scss">
.navigation {
  display: flex;
  height: 120px;
  align-items: center;

  .logo {
    display: block;
    background-image: url('../assets/images/storelink-logo.svg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: contain;
    height: 35px;
    width: 170px;
  }

  .menu {
    margin-left: auto;
    display: flex;
    align-items: center;
    justify-content: center;

    .menu-btn {
      display: block;
      background-image: url('../assets/images/menu.svg');
      background-repeat: no-repeat;
      background-position: center center;
      background-size: contain;
      height: 40px;
      width: 40px;
    }

    .menu-close {
      background-image: url('../assets/images/close-menu.svg');
    }
  }
}

.menu-items {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  border-bottom: 1px solid #e3e3e3;

  .menu-item {
    width: 50%;
    color: $white;
    font-size: 1.5em;
    font-weight: 500;

    &:hover {
      color: $primary;
      
    }
  }
}

.sub-menu-items {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  .sub-menu-group {
    width: 20%;
    color: $white;
  }
}

.menu-content {
  background-color: #000;
  height: 100vh;
}
</style>