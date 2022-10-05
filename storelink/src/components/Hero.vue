<template>
  <div class="page hero">
    <div class="container">
      <h1 class="hero-display mt-1">We build successful brands across a wide range of retail channels.</h1>

      <div class="hero-btns mt-3">
        <a href="#" class="btn btn-primary btn-lg mr-1 uppercase small">WHAT WE DO</a>
        <a href="#" class="btn btn-lg btn-outline uppercase small">MAKE AN ENQUIRY</a>
      </div>

      <div class="hero-content mt-2">
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Debitis labore eos a eaque delectus. Eum distinctio ad accusamus quaerat facilis!</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style lang="scss" scoped>
.hero {
  background-image: url('../assets/images/home-hero@2x.jpg');
  background-position: top center;
  background-size: 100% 100%;
  
  .hero-display {
    display: block;
  }

  .hero-btns {
    display: flex;
  }

  .hero-content {
    width: 70%;
  }
}
</style>