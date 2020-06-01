<template>
  <div class="hello">
    <div class="container">
      <div class="row">
        <div class="col-12"><h3>Sökresultat</h3></div>
      </div>
    </div>
    <b-container>
      <b-row align-v="center">
        <PhotoContainer v-bind="pics"></PhotoContainer>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import PhotoContainer from "@/components/PhotoContainer.vue";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: { PhotoContainer },
  mounted() {
    this.fetchData();
  },
  data() {
    return {
      pics: []
    };
  },
  methods: {
    async fetchData() {
      const res = await fetch("http://localhost:8080/BothniaBackEnd/resources/picture?id=1");
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
