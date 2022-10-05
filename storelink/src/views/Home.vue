<template>
  <div class="home">
    <Hero/>
    <Coverage />
    <Channels />
    <Fields />
    <Brands />
  </div>
</template>

<script>
import Hero from '@/components/Hero'
import Coverage from '@/components/Coverage'
import Channels from '@/components/Channels'
import Fields from '@/components/Fields'
import Brands from '@/components/Brands'

export default {
  name: 'Home',
  components: {
    Hero,
    Coverage,
    Channels,
    Fields,
    Brands
  }
}
</script>

<style scoped>
.home {
  margin-top: -140px;
}
</style>