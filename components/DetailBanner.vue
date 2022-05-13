<template>
  <div>
    <div class="shadow overflow-hidden ml-3 mt-4 mb-5">
      <div class="wrapper">
        <div class="row">
          <div class="col">
            <div class="row">
              <div class="col-auto">
                <div class="company-logo d-flex align-items-center rounded">
                  <img src="https://aday-spage.mncdn.com/Knet_img_bag-with-gray-bg.6e8e6ff.svg?v=p0509103751962" alt="">
                </div>
              </div>
              <div class="col no-gutters">
                <div class="with-padding">
                  <div class="title">{{ data.companyName }}</div>
                  <div class="text">
                    {{ data.department }}
                  </div>
                  <div class="follow">
                    Takip et
                  </div>
                </div>
              </div>
            </div>
            <div class="info">
              Şirket Aydınlatma Metni
            </div>
            <div class="info-text overflow-hidden mt-1">
              KİŞİSEL VERİLERİN ELDE EDİLMESİ VE İŞLENMESİ İLE İLGİLİ BİLGİLENDİRME
            </div>
            <div class="follow mt-3">
              Detaylı Bilgi
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="shadow overflow-hidden ml-3 mt-5 mb-5">
      <div class="wrapper">
        <div class="col-auto">
          <div class="p-3 d-flex align-items-center justify-content-center rounded">
            <img src="https://tpc.googlesyndication.com/simgad/7094440557405609044" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "DetailBanner",
  props: ["data"]
};
</script>

<style scoped>
.shadow {
  background-color: white;
  border-radius: 4px;
  box-shadow: 0 1px 5px 0 rgb(0 0 0 / 10%);
  padding: 1rem !important;
}

.info {
  font-weight: bold;
  margin-top: 20px;
}

.text {
  color: #686868;
  font-size: 13px;
}

.follow {
  color: #8316b5;
  cursor: pointer;
  font-size: 14px;
}

.company-logo {
  background-color: #fff;
  border: 1px solid #dee2e6;
  height: 58px;
  overflow: hidden;
  padding: 0.25rem;
  width: 58px;
}
</style>
