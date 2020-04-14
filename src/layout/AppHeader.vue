<template>
  <header class="header-global">
    <div>
      <!-- TITRE -->
      <b-row>
        <div class="row justify-content-center title" style="background: #4fb68d">
          <h1 class="text-white font-weight-bold">Mon beau lapin</h1>
        </div>
      </b-row>
      <!-- MENU DEROULANT -->
      <b-row>
        <base-nav
          class="navbar-main col-md-12"
          transparent
          type
          effect="light"
          expand
          style="top: 8vw; background: #4fb68d"
        >
          <div class="container">
            <div class="row" slot-scope="{closeMenu}">
              <div class="col-md-6 collapse-brand">
                <!-- <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/%22%3E
              <img src="img/brand/blue.png" />
                </a>-->
              </div>
              <div class="col-md-3 collapse-close">
                <close-button @click="closeMenu"></close-button>
              </div>
            </div>
          </div>

          <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
            <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
              <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
                <i class="ni ni-ui-04 d-lg-none"></i>
                <span class="nav-link-inner--text">Généralités</span>
              </a>
              <div class="dropdown-menu-inner">
                <router-link to="landing" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Journée type du lapin</h6>
                  </div>
                </router-link>

                <a href="#" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Du jardin à l'urbain</h6>
                  </div>
                </a>
                <a href="#" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Un lapin dans la ville</h6>
                  </div>
                </a>
                <a href="#" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Espérance de vie du lapin</h6>
                  </div>
                </a>
                <a href="#" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Adopter un lapin</h6>
                  </div>
                </a>
                <a href="#" class="media d-flex align-items-center">
                  <div class="media-body ml-2">
                    <h6 class="heading text-primary mb-md-1">Préparer l'arrivée de mon lapin</h6>
                  </div>
                </a>
              </div>
            </base-dropdown>

            <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
              <i class="ni ni-collection d-lg-none"></i>
              <span class="nav-link-inner--text">Habitat</span>
            </a>

            <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
              <i class="ni ni-collection d-lg-none"></i>
              <span class="nav-link-inner--text">Alimentation</span>
            </a>

            <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
              <i class="ni ni-collection d-lg-none"></i>
              <span class="nav-link-inner--text">Santé</span>
            </a>

            <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
              <i class="ni ni-collection d-lg-none"></i>
              <span class="nav-link-inner--text">Contact</span>
            </a>
          </ul>
        </base-nav>
      </b-row>
    </div>

    <!-- BANNIERE -->
    <div class="container-fluid">
      <img src="../../public/img/images/banniere2.jpg" class="img-fluid" alt="Responsive image" />
    </div>
  </header>
</template>

<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  }
};
</script>

<style>
.text-white {
  padding-top: 1vw;
  font-size: 6.5vw;
  font-family: "polTangerine", "Comic Sans MS", serif;
}
.navbar-main {
  padding-top: 0 !important;
  padding-bottom: 0 !important;
  margin-top: 20px;
}
span {
  font-size: 20px;
  font-family: "polYrsa", "Comic Sans MS", serif;
}
img {
  padding-top: 35px;
  margin-bottom: -5px;
}
.container-fluid {
  padding: 0 !important;
}
.title {
  margin-right: 0 !important;
}

/* TELEPHONE*/
@media screen and (max-width: 768px) {
  .navbar-toggler {
    margin-top: -40px;
  }
  .text-white {
    padding-top: 10px;
    font-size: 9vw;
  }
  .img-fluid {
    padding-top: 0;
  }
  .container {
    display: none;
  }
}
</style>
