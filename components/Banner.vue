<template>
  <div class="widget mt-4">
    <div class="content p-4 pt-5">
      <div class="text-wrapper">
        <span class="text">
          Kariyer.net’te özgeçmişin yok mu?
        </span>
      </div>
      <div class="login-now">
        <span href="#" class="login-link">
          Hemen Üye Ol
        </span>
      </div>
      <div class="row line-block mx-n4 py-3">
        <div class="p-0 col">
          <div class="d-flex position-relative">
            <hr>
            <div class="k-text line d-flex justify-content-center align-items-center bg-white medium">
              veya
            </div>
            <hr>
          </div>
        </div>
      </div>
      <div class="button-block">
        <div class="row pb-1">
          <div class="col">
            <button class="btn login-button w-100 shadow-none btn-primary">Giriş Yap</button>
          </div>
        </div>
        <div class="row login-with-facebook pt-2">
          <div class="col">
            <div>
              <button type="button" class="btn shadow-none btn-outline-facebook btn-block">
                <div class="row justify-content-center no-gutters align-items-center">
                  <div class="col-auto">
                  </div>
                  <div class="col-auto text-sm-center">
                    Facebook ile Giriş Yap
                  </div>
                </div>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner"
};
</script>

<style scoped>
.widget {
  border-radius: 4px;
  box-shadow: 0 1px 5px 0 rgb(0 0 0 / 10%);
}

.text-wrapper {
  align-items: center;
  display: flex;
  justify-content: center;
}

.text {
  color: #333;
  font-size: 1rem;
  font-weight: 700;
  line-height: 1.2;
  text-align: center;
}

.login-now {
  color: #8316b5;
  cursor: pointer;
  font-size: 10px;
  text-align: center;
  margin-top: 10px;
}

.login-now:hover {
  text-decoration: underline !important;
}

.k-text {
  color: #878787;
  min-width: 48px;
}

.btn-outline-facebook {
  border-color: #3b5998;
  color: #3b5998;
}

.btn-outline-facebook:hover {
  background-color: #3b5998;
  color: #fff;
}

.btn-primary {
  background-color: #8316b5;
  border-color: #8316b5;
  color: #fff;
}
</style>
