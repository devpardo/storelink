<template>
  <div class="page brands">
    <div class="container pt-4">
      <h3 class="small uppercase text-center text-primary mb-5">Brands we work with</h3>

      <ul class="items mb-5">
        <li class="item text-center" :class="item.slug" v-for="(item, index) in items" :key="index" />
      </ul>

      <div class="mt-5 pt-3 mb-1 footer">
        <div class="footer-part">
          <a href="#" class="logo mt-2 ml-3 mb-2"></a>
          <a href="#" class="fb-link ml-3"></a>
        </div>
        <div class="footer-part footer-links">
          <div class="link-groups">
            <ul>
              <li>Home</li>
              <li>The Storelink Difference</li>
              <li>What we do</li>
              <li>Services</li>
              <li>Building Brands</li>
              <li>Partners</li>
              <li>Retailers</li>
            </ul>
          </div>
          <div class="link-groups">
            <ul>
              <li>New Business Enquiries</li>
              <li>Our Team</li>
              <li>About Us</li>
              <li>Latest News</li>
              <li>Careers</li>
              <li>Contact Us</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="text-center uppercase small copyright">
        Copyright storelink 2022. web design by brownpaperbag
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Brands',
  data() {
    return {
      items : [
        { slug: 'simply-good' },
        { slug: 'natures-organic' },
        { slug: 'sanitarium' },
        { slug: 'mum' }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.brands {
  background-color: #000;
  height: 100vh;

  .items {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;

    .item {
      width: 20%;
      height: 70px;
      background-position: center center;
      background-repeat: no-repeat;
      background-size: 60%;
      
    }

    .simply-good {
      background-image: url('../assets/images/simply-good-logo.png');
    }
    
    .natures-organic {
      background-image: url('../assets/images/natures-organic-logo.png');
    }

    .sanitarium {
      background-image: url('../assets/images/sanitarium-logo.png');
    }

    .mum {
      background-image: url('../assets/images/mum-logo.png');
    }

  }

  
}

@keyframes marquee {
  0% {
  transform: translateX(100%);
  }
  100% {
  transform: translateX(-100%);
  }
} 

.footer {
  border-top: 1px solid #525252;
  border-bottom: 1px solid #525252;

  display: flex;

  .logo {
    display: block;
    background-image: url('../assets/images/storelink-logo.svg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: contain;
    height: 35px;
    width: 100px;
  }

  .fb-link {
    display: block;
    background-image: url('../assets/images/fb-icon.svg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: contain;
    height: 70px;
    width: 70px;
  }

  .footer-part {
    width: 50%;
    height: 40vh;
  }

  .footer-links {
    display: flex;
    
    .link-groups {
      width: 50%;
      line-height: 1.85em;
    }
  }
}

.copyright {
  font-size: .65em;
  color: #525252;
  font-weight: bolder;
}
</style>