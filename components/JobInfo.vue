<template>
  <div>
    <div class="shadow overflow-hidden mt-4">
      <div class="row">
        <div class="col">
          <div class="title-wrapper">
            <h2 class="title">
              {{ data.positionName }}
            </h2>
            <div class="detail">{{ data.companyName }}</div>
            <div class="mt-4">
              <span class="location mr-2">{{ data.cityName }}</span>
              <span class="all">Tümünü Gör</span>
            </div>
          </div>
        </div>
        <div class="col d-flex justify-content-end">
          <div class="buttons">
            <button
              class="btn btn-primary btn-apply mr-1 d-lg-inline-block d-none"
            >
              Başvur
            </button>
            <button
              class="btn btn-save btn-outline-primary mr-1 d-lg-inline-block d-none"
            >
              Kaydet
            </button>
          </div>
        </div>
      </div>
      <div class="bottom-section">
        <div class="row space-row">
          <div class="col">
            <div class="bottom-title">Çalışma Şekli</div>
            <div class="bottom-text">{{ data.wayWorking }}</div>
          </div>
          <div class="col">
            <div class="bottom-title">Pozisyon Seviyesi</div>
            <div class="bottom-text">{{ data.positionLevel }}</div>
          </div>
          <div class="col">
            <div class="bottom-title">Departman</div>
            <div class="bottom-text">{{ data.department }}</div>
          </div>
          <div class="col">
            <div class="bottom-title">Başvuru Sayısı</div>
            <div class="bottom-text">{{ data.applyNumber }} Başvuru</div>
          </div>
        </div>
      </div>
    </div>
    <div class="shadow overflow-hidden mt-5 mb-5">
      <div class="mb-2 font-weight-bold">
        GENEL NİTELİKLER VE İŞ TANIMI
      </div>
      <div class="mb-2 font-weight-bold">
        {{ data.jobRequirements }}
      </div>
      <ul class="mt-5">
        <li v-for="item in data.requirementsContent" :key="data.jobId">{{ item }}</li>
      </ul>
      <div class="ml-3 work-title">İŞ TANIMI</div>
      <div class="mt-2 font-weight-bold">
        İş Tanımı:
      </div>
      <ul class="mt-3">
        <li v-for="item in data.jobDescription" :key="data.jobId">{{ item }}</li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: "JobInfo",
  props: ["data"]
};
</script>

<style scoped>
.shadow {
  box-shadow: 0 1px 5px 0 rgb(0 0 0 / 10%);
  border-radius: 4px;
  background-color: white;
  padding: 1rem !important;
}

.work-title {
  margin-top: 70px;
  margin-bottom: 40px;
}

.bottom-title {
  font-size: 14px;
  color: #686868;
  font-weight: 400;
}

.bottom-text {
  color: #333;
  font-size: 14px;
  font-weight: 500;
  line-height: 1.43;
}

.bottom-section {
  padding: 1rem !important;
  margin-top: 15px;

  background-color: #f8f9fa;
  border-radius: 4px;
}

.space-row {
  display: flex;
  justify-content: space-between;
}

.all {
  color: #8316b5;
  cursor: pointer;
  font-weight: 400;
  font-size: 14px;
}

.title {
  font-size: 17px;
  font-weight: 700;
}

.detail {
  font-weight: 400;
}

.location {
  font-size: 14px;
  font-weight: 400;
  margin-top: 15px;
  opacity: 0.5;
}

.btn {
  background-color: #8316b5;
  border-color: #8316b5;
  font-weight: 500;
  max-width: 140px;
  min-width: 110px;
  width: 12vw;
}

.btn-apply:hover {
  background-color: #6f42c1;
}

.btn-save {
  color: #8316b5;
  background-color: #fff;
  border-color: #8316b5;
}
</style>
