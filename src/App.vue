<template>
  <div class="container-fluid main">
    <div class="row imgBg">
      <div class="marBg col-sm-4 col-md-3" />
      <div class="titleDetails">
        <h1>Explore</h1>
        <div class="moreDetails" :class={} data-bs-toggle="modal" data-bs-target="#exampleModal" >
          <img class="moreBtn" src="./assets/Plus.svg"/>
          <p>More Details</p>
        </div>
      </div>
      <div class="socials col-8">
        <img class="facebook" src="./assets/Facebook.svg" />
        <img class="instagram" src="./assets/Instagram.svg" />
      </div>
    </div>
    <ExploreModal title="Explore" :body="modalBody"/>
  </div>
</template>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

<script>
import ExploreModal from './components/ExploreModal.vue'

const modalBody = 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim adminima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur?'

export default {
  name: 'App',
  components: {
    ExploreModal
  },
  data() {
    return {
      modalBody,
    }
  },
  methods: {
    removeMainTitle() {
      
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  /*padding-top: 60px;*/
}

.main {
  /*background: #611818;*/
  height: 100vh;
  width: 100vw;
}

.marBg {
  background: #611818;
  height: 100vh;
}

.imgBg {
  background-image: url('./assets/Forest.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100vh;
}

.titleDetails {
  width: auto;
  position: absolute;
  text-align: left;
  top: 50%;
  left: 15%;
}

.titleDetails h1 {
  font-size: 4rem;
  font-family: 'Libre Bodoni', serif;
}

.moreDetails {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
}

.moreDetails:hover {
  cursor: pointer;
}

.moreDetails p {
  margin-left: 15px;
  margin-bottom: 0;
}

.moreBtn {
  height: 35px;
  width: 35px;
}

.moreBtn:hover {
  cursor: pointer;
}

.socials {
  position: absolute;
  bottom: 0;
  right: 0;
  display: flex;
  flex-flow: column nowrap;
  align-items: flex-end;
}

.socials img {
  height: 50px;
  width: 50px;
  margin: 15px 0;
}

@media (min-width: 692px) {
  .titleDetails h1 {
    font-size: 7rem;
  }

  .moreDetails {
    margin-left: 35px;
  }
}

@media (min-width: 962px) {
  .titleDetails h1 {
    font-size: 10rem;
   }
}

</style>
