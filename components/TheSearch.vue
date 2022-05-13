<template>
  <div class="col-12 position-sticky mt-xl-5 wrapper">
    <div id="desktop-search-bar" class="search-layout d-none d-sm-block" style="margin-top: 0;">
      <div class="px-0 container">
        <div class="d-none d-md-block">
          <div class="row">
            <div id="search-top" class="col-sm-12 col-md-12 col-8">
              <div class="search-box">
                <div class="search-wrapper">
                  <div class="k-global-job-search">
                    <form>
                      <div class="row no-gutters">
                        <div class="col-7">
                          <div class="mr-2">
                            <input @keyup="filteredJoblist('positionName',search.position)"
                                   v-model="search.position"
                                   type="text"
                                   placeholder="Pozisyon veya şirket ara" autocomplete="off" maxlength="200" value=""
                                   class="form-control">
                          </div>
                        </div>
                        <div class="col-5">
                          <div class="row no-gutters">
                            <div class="col">
                              <div class="mr-2">
                                <input @keyup="filteredJoblist('cityName',search.city)" v-model="search.city"
                                       type="text"
                                       placeholder="Şehir veya ilçe ara" autocomplete="off" maxlength="200" value=""
                                       class="form-control" />
                              </div>
                            </div>
                            <div class="col-auto">
                              <div class="search-button-wrapper d-lg-block">
                                <button type="submit" class="btn shadow-none btn-primary btn-block">
                                  İş Ara
                                </button>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </form>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheSearch",
  props: ["filteredJoblist"],
  data() {
    return {
      search: {
        city: "",
        position: ""
      }
    };
  }
};
</script>

<style scoped>
.wrapper {
  position: sticky;
  padding-right: 0;
  padding-left: 0;
  margin-top: 0 !important;
  top: 0;
  z-index: 9999;
}

#desktop-search-bar {
  transition: padding .2s ease-in-out;
}

.search-layout {
  background: #fff;
  box-shadow: 0 4px 5px 0 rgb(0 0 0 / 10%);
}

.search-layout:hover {
  box-shadow: 0 4px 5px 0 rgb(0 0 0 / 20%);
}

.row {
  display: flex;
  flex-wrap: wrap;
  margin-right: -15px;
  margin-left: -15px;
}

#search-top {
  position: relative;
  z-index: 2;
}

.search-box {
  padding-bottom: 15px;
  padding-top: 15px;
  transition: all .2s ease-in-out;
  width: 100%;
}

.search-box .search-wrapper {
  max-width: 750px !important;
  transition: all .2s ease-in-out;
}

.no-gutters {
  margin-right: 0;
  margin-left: 0;
}

.btn {
  background-color: #8316b5 !important;
  border: 1px solid transparent;
  width: 89px;
}
</style>
