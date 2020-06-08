<template>
  <div id="app">
    <header>
      <div id="nav">
        <ul class="nav justify-content-end">
          <li class="nav-item">
            <b-button v-b-tooltip.hover title="Om" variant="light" href="/about"
              >Om</b-button
            >
          </li>
          <li class="nav-item">
            <b-button
              v-b-tooltip.hover
              title="Logga in"
              variant="light"
              v-b-modal="modalId"
              data-toggle="modal"
              data-target="#modalLRForm"
              >Logga in</b-button
            >
          </li>
          <li class="nav-item">
            <b-button v-b-tooltip.hover title="Hjälp" variant="light" href="/"
              >Hjälp</b-button
            >
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
      <div>
        <SearchBar></SearchBar>
      </div>
      <!--Modal: Login / Register Form-->
      <div
        class="modal fade"
        id="modalLRForm"
        tabindex="-1"
        role="dialog"
        aria-labelledby="myModalLabel"
        aria-hidden="true"
      >
        <div class="modal-dialog cascading-modal" role="document">
          <!--Content-->
          <div class="modal-content">
            <!--Modal cascading tabs-->
            <div class="modal-c-tabs">
              <!-- Nav tabs -->
              <ul
                class="nav nav-tabs md-tabs tabs-2 light-blue darken-3"
                role="tablist"
              >
                <li class="nav-item">
                  <a
                    class="nav-link active"
                    data-toggle="tab"
                    href="#panel7"
                    role="tab"
                    ><i class="fas fa-user mr-1"></i> Login</a
                  >
                </li>
                <li class="nav-item">
                  <a
                    class="nav-link"
                    data-toggle="tab"
                    href="#panel8"
                    role="tab"
                    ><i class="fas fa-user-plus mr-1"></i> Register</a
                  >
                </li>
              </ul>

              <!-- Tab panels -->
              <div class="tab-content">
                <!--Panel 7-->
                <div
                  class="tab-pane fade in show active"
                  id="panel7"
                  role="tabpanel"
                >
                  <!--Body-->
                  <div class="modal-body mb-1">
                    <div class="md-form form-sm mb-5">
                      <i class="fas fa-envelope prefix"></i>
                      <input
                        type="email"
                        id="modalLRInput10"
                        class="form-control form-control-sm validate"
                      />
                      <label
                        data-error="wrong"
                        data-success="right"
                        for="modalLRInput10"
                        >Your email</label
                      >
                    </div>

                    <div class="md-form form-sm mb-4">
                      <i class="fas fa-lock prefix"></i>
                      <input
                        type="password"
                        id="modalLRInput11"
                        class="form-control form-control-sm validate"
                      />
                      <label
                        data-error="wrong"
                        data-success="right"
                        for="modalLRInput11"
                        >Your password</label
                      >
                    </div>
                    <div class="text-center mt-2">
                      <button class="btn btn-info">
                        Log in <i class="fas fa-sign-in ml-1"></i>
                      </button>
                    </div>
                  </div>
                  <!--Footer-->
                  <div class="modal-footer">
                    <div class="options text-center text-md-right mt-1">
                      <p>
                        Not a member? <a href="#" class="blue-text">Sign Up</a>
                      </p>
                      <p>Forgot <a href="#" class="blue-text">Password?</a></p>
                    </div>
                    <button
                      type="button"
                      class="btn btn-outline-info waves-effect ml-auto"
                      data-dismiss="modal"
                    >
                      Close
                    </button>
                  </div>
                </div>
                <!--/.Panel 7-->

                <!--Panel 8-->
                <div class="tab-pane fade" id="panel8" role="tabpanel">
                  <!--Body-->
                  <div class="modal-body">
                    <div class="md-form form-sm mb-5">
                      <i class="fas fa-envelope prefix"></i>
                      <input
                        type="email"
                        id="modalLRInput12"
                        class="form-control form-control-sm validate"
                      />
                      <label
                        data-error="wrong"
                        data-success="right"
                        for="modalLRInput12"
                        >Your email</label
                      >
                    </div>

                    <div class="md-form form-sm mb-5">
                      <i class="fas fa-lock prefix"></i>
                      <input
                        type="password"
                        id="modalLRInput13"
                        class="form-control form-control-sm validate"
                      />
                      <label
                        data-error="wrong"
                        data-success="right"
                        for="modalLRInput13"
                        >Your password</label
                      >
                    </div>

                    <div class="md-form form-sm mb-4">
                      <i class="fas fa-lock prefix"></i>
                      <input
                        type="password"
                        id="modalLRInput14"
                        class="form-control form-control-sm validate"
                      />
                      <label
                        data-error="wrong"
                        data-success="right"
                        for="modalLRInput14"
                        >Repeat password</label
                      >
                    </div>

                    <div class="text-center form-sm mt-2">
                      <button class="btn btn-info">
                        Sign up <i class="fas fa-sign-in ml-1"></i>
                      </button>
                    </div>
                  </div>
                  <!--Footer-->
                  <div class="modal-footer">
                    <div class="options text-right">
                      <p class="pt-1">
                        Already have an account?
                        <a href="#" class="blue-text">Log In</a>
                      </p>
                    </div>
                    <button
                      type="button"
                      class="btn btn-outline-info waves-effect ml-auto"
                      data-dismiss="modal"
                    >
                      Close
                    </button>
                  </div>
                </div>
                <!--/.Panel 8-->
              </div>
            </div>
          </div>
          <!--/.Content-->
        </div>
      </div>
      <!--Modal: Login / Register Form-->
    </header>
    <router-view />
  </div>
</template>

<script>
import Vue from "vue";
import SearchBar from "./components/SearchBar";
Vue.component("SearchBar", SearchBar);
export default {
  computed: {
    modalId() {
      return `modal-${this.id}`;
    }
  },
  data() {
    return{}
  }
};
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
  btn {
    background-color: white;
  }
}

#menu {
  padding: 10px;
}

header {
  background-color: white;
}
</style>
