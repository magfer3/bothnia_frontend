<template>
  <div class="hello">
    <div class="container">
      <div class="row">
        <div class="col-12"><h3>Populärt</h3></div>
      </div>
    </div>
    <b-container>
      <b-row align-v="center">
        <PhotoContainer
          v-for="pic in picsPopular"
          :key="pic.piNo"
          :piNo="pic.piNo"
          :locationOnDisc="pic.locationOnDisc"
          ></PhotoContainer>
      </b-row>
    </b-container>
    <div class="container">
      <div class="row">
        <div class="col-12"><h3>Senaste nytt</h3></div>
      </div>
    </div>
    <b-container>
      <b-row align-v="center">
        <PhotoContainer
          v-for="pic in picsRecent"
          :key="pic.piNo"
          :piNo="pic.piNo"
          :locationOnDisc="pic.locationOnDisc"
        ></PhotoContainer>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import PhotoContainer from "@/components/PhotoContainer.vue";

export default {
  name: "HomePage",
  props: {
    msg: String
  },
  components: { PhotoContainer },
  mounted() {
    this.fetchDataPopular();
    this.fetchDataRecent();
  },
  data() {
    return {
      picsRecent: [],
      picsPopular: []
    };
  },
  methods: {
    async fetchDataPopular() {
      var res = await fetch(
        "http://localhost:8080/BothniaBackEnd/resources/picture/pictures?search=djur"
      );
      var val = await res.json();
      this.picsPopular = val;
    },
    async fetchDataRecent() {
      var res = await fetch(
        "http://localhost:8080/BothniaBackEnd/resources/picture/pictures?search=sport"
      );
      var val = await res.json();
      this.picsRecent = val;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 50px 0;
  text-align: left;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

#hello {
  text-align: left;
}
</style>
