<template>
  <footer class="footer has-cards">
    <div class="container">
      <div class="row align-items-center justify-content-md-between">
        <div class="col-md-6">
          <div class="copyright">
            &copy; {{year}}
            Tous droits réservés.
          </div>
        </div>
        <div class="col-md-6">
          <ul class="nav nav-footer justify-content-end">
            <li class="nav-item">
              <a
                target="_blank"
                rel="noopener"
                href="https://twitter.com/creativetim"
                class="btn btn-neutral btn-icon-only btn-twitter btn-round btn-lg"
                data-toggle="tooltip"
                data-original-title="Follow us"
                title="twitter"
              >
                <i class="fa fa-twitter"></i>
              </a>
            </li>
            <li class="nav-item">
              <a
                target="_blank"
                rel="noopener"
                href="https://www.facebook.com/creativetim"
                class="btn btn-neutral btn-icon-only btn-facebook btn-round btn-lg"
                data-toggle="tooltip"
                data-original-title="Like us"
              >
                <i class="fa fa-facebook-square"></i>
              </a>
            </li>
            <li class="nav-item">
              <a
                target="_blank"
                rel="noopener"
                href="https://dribbble.com/creativetim"
                class="btn btn-neutral btn-icon-only btn-dribbble btn-lg btn-round"
                data-toggle="tooltip"
                data-original-title="Follow us"
              >
                <i class="fa fa-dribbble"></i>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  name: "app-footer",
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style>
.footer {
  background-color: #e8ffe6;
}
</style>
