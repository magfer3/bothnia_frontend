<template>
  <div class="hello">
    <div class="container">
      <div class="row">
        <div class="col-12"><h3>Sökresultat</h3></div>
      </div>
    </div>
    <b-container>
      <b-row align-v="center">
        <PhotoContainer
          v-for="pic in pics"
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
  name: "SearchPage",
  components: { PhotoContainer },
  created() {
    this.fetchData();
  },
  data() {
    return {
      pics: [],
      searchText: ""
    };
  },
  watch: {
    '$route': 'fetchData'
  },
  methods: {
    getSearchText(searchText) {
      var searchTextArr = searchText.split(" ");
      console.log(searchTextArr);
      var searchTextString = searchTextArr.join('_');
      console.log(searchTextString);
      return searchTextString;
    },
    async fetchData() {
      this.searchText = this.getSearchText(this.$route.query.prop);
      const res = await fetch(
        "http://localhost:8080/BothniaBackEnd/resources/picture/pictures?search=" +
          this.searchText
      );
      const val = await res.json();
      this.pics = val;
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
