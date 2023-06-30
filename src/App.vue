<template>
  <div id="app">
    <!-- blog-detatils -->

    <div id="app" class="blog-details center">
      <div class="blog-details__info">
        <component :is="changeTabs"></component>

      </div>

      <div class="blog-details__tags">
        <h2 class="blog-details__tags__heading textAlignLeft">Tags</h2>


        <div class="blog-details__tags__buttons">

          <button class="blog-details__tags__buttons__btn" @click="currentTab = nameButton"
            v-for="nameButton in nameButtons" :key="nameButton.id">
            {{ nameButton }}
          </button>
        </div>
      </div>


    </div>



  </div>
</template>

<script>
import ChangeKitchen from './components/ChangeKitchen.vue'
import ChangeBedroom from './components/ChangeBedroom.vue'
import ChangeBuilding from './components/ChangeBuilding.vue'
import ChangeArchitecture  from './components/ChangeArchitecture.vue'
import ChangeKitchenPlanning from './components/ChangeKitchenPlanning.vue'

export default {
  name: 'App',
  components: {
    ChangeKitchen,
    ChangeBedroom,
    ChangeBuilding,
    ChangeArchitecture,
    ChangeKitchenPlanning

  },
  data() {
    return {
      nameButtons: ['Kitchen', 'Bedroom', 'Building', 'Architecture', 'KitchenPlanning', 'Bedroom'],
      currentTab: 'Kitchen'
    }
  },
  computed: {
    changeTabs() {
      return `Change${this.currentTab}`;
    }
  },
}
</script>

<style lang="scss">

$widthSite-laptop: 1201px;
$widthSite-laptop-center: $widthSite-laptop / 2;
$colorHeader: #292F36;
$colorText: #4D5053;
$colorWhite: #FFFFFF;
$colorBackground: #F4F0EC;
$colorCounterBlock: #CDA274;
$colorBlock: #F4F0EC;

.blog-details {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 40px;

  &__info {
    grid-column-start: 1;
    grid-column-end: 3;
  }

  &__tags {
    &__heading {
      margin-bottom: 25px;
    }

    &__buttons {
      display: flex;
      justify-content: flex-start;
      flex-wrap: wrap;
      gap: 8px;



      &__btn {
        color: $colorHeader;
        background-color: $colorBlock;
        font-family: Jost;
        font-size: 18px;
        font-weight: 400;
        line-height: 23px;
        letter-spacing: 0.02em;
        padding: 9px 30px;
        border-radius: 10px;
        border: none;
        cursor: pointer;

        &:hover {
          color: $colorWhite;
          background-color: $colorHeader;
        }
      }
    }
  }
}
</style>
