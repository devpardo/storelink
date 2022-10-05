<template>
  <div class="page fields">
    <div class="container">
      <div class="cards mt-4">

        <div v-for="(item, index) in items" :key="index" class="card pa-1">
          <div class="card-content">
              <div class="card-content-title mb-4 pa-1">
                <span class="icon mr-1" :class="item.icon_slug">
                </span>
                <small class="uppercase card-text-title">{{ item.title }}</small>
              </div>
              <div class="card-text small pa-1">
                {{ item.content }}
              </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Fields',
  data() {
    return {
      items: [
        { icon_slug: 'field-sales', title: 'Field Sales', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'},
        { icon_slug: 'fmcg-consult', title: 'Key account management', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'},
        { icon_slug: 'data-insights', title: 'Data Insights', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'},
        { icon_slug: 'freight-warehousing', title: 'Freight & Warehousing', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'},
        { icon_slug: 'custom-merch', title: 'Custom Merchandising Solutions', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'},
        { icon_slug: 'fmcg-consult', title: 'fmcg consultancy', content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Expedita, soluta modi dicta sit praesentium adipisci perspiciatis omnis beatae autem deserunt veritatis nihil, porro maxime quis ipsa. Enim iusto earum hic!'}
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.fields {
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
      width: calc(100%/3);
      height: calc(50vh - 70px);
      box-sizing: border-box;

      .card-content {
        text-align: left;
        background-color: transparent;
        color: #fff;
        height: 100%;
        border-radius: 4px;
        border: 1px solid $white;
        overflow: auto;

        .card-content-title {
          display: flex;
          align-items: center;

          .icon {
            height: 40px;
            width: 40px;
            background-position: center center;
            background-repeat: no-repeat;
          }

          .field-sales {
            background-image: url('../assets/images/field-sales.svg');
          }

          .data-insights {
            background-image: url('../assets/images/data-insights.svg');
          }

          .custom-merch {
            background-image: url('../assets/images/custom-merch.svg');
          }

          .fmcg-consult {
            background-image: url('../assets/images/fmcg-consult.svg');
          }

          .freight-warehousing {
            background-image: url('../assets/images/freight-warehousing.svg');
          }
        }

        .card-text-title {
          font-weight: 400;
        }

        .card-text {
          font-size: .65em;
          line-height: 1.5em;
          text-align: justify;
        }
      }
    }

    
  }
}
</style>