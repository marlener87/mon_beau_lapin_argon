<template>
  <footer class="footer">
    <div class="container foot">
      <div class="row align-items-center justify-content-between">
        <div class="col-md-8">
          <div class="copyright">
            &copy; {{year}}
            Tous droits réservés.
          </div>
        </div>
        <div class="col-md-4">
          <ul class="list-unstyled d-inline-flex img-fluid">
            <li>
              <a href="https://twitter.com/?lang=fr" target="_blank">
                <img
                  src="../../public/img/images/reseaux_sociaux/twitter.png"
                  title="twitter"
                  class="imgFooter"
                />
              </a>
            </li>
            <li>
              <a href="https://www.instagram.com/?hl=fr" target="_blank">
                <img
                  src="../../public/img/images/reseaux_sociaux/instagram.png"
                  title="instagram"
                  class="imgFooter"
                />
              </a>
            </li>
            <li>
              <a
                href="https://www.facebook.com/?stype=lo&jlou=AfeGvOsiG-pTY1kUHlDRrArc6VmDCdtnuD_YTzyQPC6xqEg9ElpTI6EEHuAboUFO7Qi-o7CAuKIOyyAu2-qGm4h1XOTM2b4ci766hg2sXvVr5Q&smuh=35373&lh=Ac_NwqmF7qdcJVDH"
                target="_blank"
              >
                <img
                  src="../../public/img/images/reseaux_sociaux/social_facebook_0649.png"
                  title="facebook"
                  class="imgFooter"
                />
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
  margin-top: 0 !important;
  padding-top: 5px !important;
  padding-bottom: 30px !important;
  height: 100px !important;
  background-color: #e8ffe6 !important;
}
.imgFooter {
  padding-left: 30px;
  padding-bottom: 0 !important;
}
.foot {
  margin-left: 100px !important;
  margin-right: 100px !important;
}

/* TELEPHONE */
@media screen and (max-width: 768px) {
}
/* Ipad */
@media screen and (min-width: 768px) and (max-width: 1000px) {
  .footer {
    margin-top: 0 !important;
    padding-top: 0 !important;
    padding-bottom: 0 !important;
    height: 70px !important;
    background-color: #e8ffe6 !important;
  }
  .foot {
    margin-left: 0 !important;
    margin-right: 0 !important;
  }
}
</style>
