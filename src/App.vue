<template>
  <div id="app">
    <header>
      <div id="nav">
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <a class="nav-link active" href="/about">Om</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Logga in</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Hjälp</a>
          </li>
        </ul>
      </div>

      <div id="logo">
        <a class="navbar-brand" href="/">
          <img
            alt="Bothniabladet logo"
            src="./assets/Bothnia-logo.png"
            class="img-fluid"
          />
        </a>
      </div>
      <div id="meny">
        <router-link to="/">Nyheter</router-link> |
        <router-link to="/">Lokalt</router-link> |
        <router-link to="/">Nöje</router-link> |
        <router-link to="/">Fritid</router-link> |
        <router-link to="/">Sport</router-link>
      </div>
      <div id="searchbar">
        <router-link to="/search">Sök</router-link>
      </div>
    </header>
    <router-view />
  </div>
</template>

<script>
export default {};
</script>

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

header {
  background-color: white;
}
</style>
