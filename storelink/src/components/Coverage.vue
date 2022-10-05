<template>
  <div class="page coverage">
    <div class="container">
      <div class="cards mt-4">

        <div v-for="(item, index) in items" :key="index" class="card pa-1">
          <div class="card-content" :class="item.type">
              <div class="text-center">
                <h1 class="font-weight-light">{{ item.title }}</h1>
                <small class="uppercase font-weight-bold">{{ item.subtitle }}</small>
              </div>
          </div>
        </div>
       
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Coverage',
  data() {
    return {
      items: [
        { title: '1,000', subtitle: 'stores covered', type: 'dark' },
        { title: '240', subtitle: 'lorem ipsum dolor', type: 'green' },
        { title: '99%', subtitle: 'of nz stores covered', type: 'light'},
        { title: '$20m', subtitle: 'lorem ipsum dolor', type: 'dark' }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.coverage {
  background-color: #000;
  height: 100vh;
  background-image: url('../assets/images/bg-glow-2.png');
  background-position: -30% 0;
  background-size: 50%;

  .cards {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    .card {
      width: 50%;
      height: calc(50vh - 70px);
      box-sizing: border-box;

      .card-content {
        background-color: $white;
        color: #000;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        border-radius: 4px;
      }

      .light {
        background-color: $white;
        color: $primary;
      }

      .dark {
        background-color: $dark;
        color: $white;
      }

      .green {
        background-color: $primary;
        color: $white;
      }
    }

    
  }
}
</style>