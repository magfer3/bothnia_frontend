<template>
  <div id="app">
    <div id="nav">
      <ul class="nav justify-content-end">
        <li class="nav-item">
          <a class="nav-link active" href="#">Om</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Logga in</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Hjälp</a>
        </li>
      </ul>
    </div>

    <div id = "logo">       
      <img alt="Bothniabladet logo" src="./assets/Bothnia-logo.png" />
    </div>
    <div id="meny">
      <router-link to="/about">Nyheter</router-link> |
      <router-link to="/about">Lokalt</router-link> |
      <router-link to="/home">Nöje</router-link> |
      <router-link to="/home">Fritid</router-link> |
      <router-link to="/about">Sport</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 10px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

#menu {
   padding: 10px;

}

</style>
