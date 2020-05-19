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
        <div class="container">
          <br />
          <div class="row justify-content-center">
            <div class="col-12 col-md-10 col-lg-8">
                <div class="card-body row no-gutters align-items-center">
                  <div class="col-auto">
                    <i class="fas fa-search h4 text-body"></i>
                  </div>
                  <!--end of col-->
                  <div class="col">
                    <input
                      class="form-control form-control-lg form-control-borderless"
                      type="search"
                      placeholder="Search topics or keywords"
                    />
                  </div>
                  <!--end of col-->
                  <div class="col-auto">
                    <router-link to="/search" tag="button" class="btn btn-lg btn-success">Search</router-link>
                  </div>
                  <!--end of col-->
                </div>
            </div>
            <!--end of col-->
          </div>
        </div>
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

.btn {
  background-color: grey;
  border: white;
}

</style>
