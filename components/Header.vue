<template>
  <header class="temp topPosition">
    <div class="row position-relative navbar-container">
      <div class="col-12">
        <div class="navbar-wrapper">
          <nav class="navbar clean-navbar-vertical-padding navbar-light navbar-expand-lg">
            <div class="clean-container-padding px-0 container">
              <ul role="menubar" class="nav main-nav-container align-items-center d-flex">
                <a href="//www.kariyer.net" target="_self" class="navbar-brand">
                  <img src="~assets/kariyernetlogo.svg" alt="kariyer.net" width="112" height="26">
                </a>
                <NuxtLink to="/joblist">
                  <li class="nav-item d-lg-block d-xl-block nav-link parent">
                    İş Ara
                  </li>
                </NuxtLink>
                <li class="nav-item d-lg-block d-xl-block nav-link parent">
                  Kariyer Rehberi
                </li>
                <li class="nav-item d-lg-block d-xl-block nav-link parent">
                  Pozisyon Rehberi
                </li>
                <li class="nav-item d-lg-block d-xl-block nav-link parent">
                  Üniversite Rehberi
                </li>
              </ul>
              <ul class="nav login-nav-container">
                <li class="nav-item user-login bg-transparent d-lg-block">
                  <button class="nav-link btn">
                    <span>ÜYE GİRİŞİ</span>
                  </button>
                </li>
                <li class="nav-item publish-ad d-xl-block d-lg-block d-xs-none">
                  <a href="/joblist" class="nav-link btn btn-purple-k-3">
                    <span class="px-4 py-2 btn">İLAN YAYINLA</span>
                  </a>
                </li>
              </ul>
            </div>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style>
.navbar-expand-lg {
  height: 60px;
}

.navbar-wrapper {
  border-bottom: 0.7px solid #ccc;
}

.temp {
  background-color: white;
  width: 100%;
  z-index: 999;
}

.main-nav-container {
  transition: all .2s ease-in-out;
}

.nav-link.parent {
  color: #000;
  display: flex;
  margin: 5px 0 0;
}

.nav-link.parent:hover {
  color: #8316b5;
}

header.temp nav .login-nav-container {
  align-items: center;
}

header.temp nav .login-nav-container .nav-item.user-login .nav-link {
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 10%), 0 1px 0 0 rgb(0 0 0 / 5%), 0 0 0 1px rgb(0 0 0 / 3%);
  padding: 0.5rem 1.5rem;
}

header.temp nav .login-nav-container .nav-item.publish-ad .nav-link {
  box-shadow: none;
  font-size: 14px;
  padding: 0.5rem 0 0.5rem 0.5rem;
}

.login-nav-container .nav-item.publish-ad .nav-link span {
  background-color: #840dc3;
  border-color: #840dc3;
  color: #fff;
  font-size: .875rem;
  font-weight: 400;
  padding: 10px;
}

.publish-ad {
  margin-left: 10px;
}

.btn {
  font-size: .875rem;
  font-weight: 700;
}
</style>
