<template>
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
                class="form-control form-control-md form-control-borderless"
                type="search"
                placeholder="Sök bilder på nyckelord"
              />
            </div>
            <!--end of col-->
            <div class="col-auto">
              <router-link to="/search" tag="button" class="btn btn-md btn-secondary">Search</router-link>
            </div>
            <!--end of col-->
          </div>
        </div>
        <!--end of col-->
      </div>
    </div>
  </div>
</template>

<script>
</script>