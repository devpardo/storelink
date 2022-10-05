<template>
  <div class="page channels">
    <div class="container">
      <div class="mt-4">

        <h6 class="uppercase small text-primary mb-3">Our Channels</h6>

        <div class="channel mb-5">
          <div class="channel-content">
            <div>
              <h3 class="mb-1">Lorem, ipsum dolor sit elit.<span class="text-primary"> Debitis consect adipisicing elit.</span> Perspiciatis ab lorem</h3>
              <a href="#" class="btn btn-lg btn-outline uppercase small">learn more</a>
            </div>
            
          </div>
          <div class="channel-content text-center">
            <div class="channel-globe">
              <a class="btn btn-lg btn-outline-primary uppercase"><h5>high tech <br> retail systems</h5></a>
            </div>
            <!-- <img :src="require('../assets/images/globe.png')" alt=""> -->
          </div>
        </div>       
      </div>
    </div>

    <div class="announcement">
      <ul class="announcement-list list-inline">
        <li class="h4">Lorem ipsum dolor sit amet.</li>
        <li class="h4">Lorem ipsum dolor sit amet.</li>
        <li class="h4">Lorem ipsum dolor sit amet.</li>
        <li class="h4">Lorem ipsum dolor sit amet.</li>
        <li class="h4">Lorem ipsum dolor sit amet.</li>
      </ul>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Channels',
  data() {
    return {
    }
  }
}
</script>

<style scoped lang="scss">
.channels {
  background-color: #000;
  height: 100vh;
  background-image: url('../assets/images/bg-glow-1.png');
  background-position: 90% 0%;
  background-size: 70%;


  .channel {
    display: flex;
    

    .channel-content {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 50%;
      height: 60vh;

      .channel-globe {
        background-image: url('../assets/images/globe.png');
        background-size: 60%;
        background-position: center center;
        background-repeat: no-repeat;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        width: 100%;
      }
    }
  }

  .announcement {
    height: 100px;
    border-top: 1px solid #e3e3e3;
    border-bottom: 1px solid #e3e3e3;
    box-sizing: border-box;
    position: relative;
    overflow: hidden;
    position: relative;

    ul> li {
      display: inline;
      margin-right: 1em;
      list-style-type: disc;
    }

    ul> li::before {
      content: '\2022';
      margin-right: .3em;
    }

    .announcement-list {
      line-height: 100px;
      position: absolute;
      width: 100%;
      height: 100%;
      margin: 0;
      text-align: left;
      animation: marquee 15s linear infinite;
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

}
</style>