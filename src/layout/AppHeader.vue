<template>
  <header class="header-global">
    <base-nav
      class="navbar-main"
      transparent
      type
      effect="light"
      expand
      style="background: #4fb68d"
    >
      <!-- TITRE -->
      <div class="container">
        <h1 class="text-white font-weight-bold">Mon beau lapin</h1>
      </div>

      <!-- MENU DEROULANT -->
      <div class="container">
        <div class="row" slot="content-header" slot-scope="{closeMenu}">
          <div class="col-12 collapse-brand">
            <a href="https://demos.creative-tim.com/vue-argon-design-system/documentation/">
              <img src="img/brand/blue.png" />
            </a>
          </div>
          <div class="col-6 collapse-close">
            <close-button @click="closeMenu"></close-button>
          </div>
        </div>

        <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
          <base-dropdown class="nav-item" menu-classes="dropdown-menu-xl">
            <a slot="title" href="#" class="nav-link" data-toggle="dropdown" role="button">
              <i class="ni ni-ui-04 d-lg-none"></i>
              <span class="nav-link-inner--text">Généralités</span>
            </a>
            <div class="dropdown-menu-inner">
              <a href="#" class="media d-flex align-items-center">
                <div class="media-body ml-2">
                  <h6 class="heading text-primary mb-md-1">Journée type du lapin</h6>
                </div>
              </a>
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
      </div>
    </base-nav>

    <!-- BANNIERE -->
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
  font-size: 80px;
  font-family: "polTangerine", "Comic Sans MS", serif;
}
span {
  font-size: 20px;
  font-family: "polYrsa", "Comic Sans MS", serif;
}
</style>
