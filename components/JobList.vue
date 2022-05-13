<template>
  <div class="list-items mt-4">
    <div v-for="joblist in data" :key="joblist.jobId">
      <a v-bind:href="'/jobdetail/'+ joblist.jobId" class="card rounded" target="_blank">
        <div class="card-content">
          <div class="row">
            <div class="col">
              <div class="row">
                <div class="col-auto">
                  <div class="company-logo d-flex align-items-center rounded">
                    <img src="https://aday-spage.mncdn.com/Knet_img_bag-with-gray-bg.6e8e6ff.svg?v=p0509103751962"
                         alt="">
                  </div>
                </div>
                <div class="col no-gutters">
                  <div class="with-padding">
                    <div class="title">{{ joblist.positionName }}</div>
                    <div class="company-name">
                      {{ joblist.companyName }}
                    </div>
                    <div class="location">
                      {{ joblist.cityName }}({{ joblist.townName }})
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col no-gutters"></div>
          <div class="bottom-section row mt-2">
            <div class="col align-items-center">
            <span class="text-bottom badge-light">
              Tam zamanlı
            </span>
            </div>
          </div>
        </div>
      </a>
    </div>
    <NoContent v-if="data.length === 0" />
  </div>
</template>

<script>
export default {
  name: "JobList",
  props: ["data"]
};
</script>

<style scoped>
.card {
  background: #fff;
  color: #333;
  display: block;
  position: relative;
  width: 100%;
}

.card:hover {
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
}

.card-content {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 131px;
  padding: 15px;
}

.rounded {
  align-items: center;
  border-radius: 4px;
  box-shadow: 0 1px 5px 0 rgb(0 0 0 / 10%);
  justify-content: center;
  margin-bottom: 15px !important;
}

.company-logo {
  background-color: #fff;
  border: 1px solid #dee2e6;
  height: 58px;
  overflow: hidden;
  padding: 0.25rem;
  width: 58px;
}

.title {
  font-size: 14px;
  font-weight: 700;
  padding: 0;
}

.no-gutters {
  padding: 0;
}

.company-name {
  color: #333;
  font-size: 12px;
  font-weight: 400;
  margin-top: -4px;
}

.location {
  color: grey;
  font-size: 12px;
}

.bottom-section {
  align-items: center;
  display: flex !important;
  justify-content: flex-start;
}

.text-bottom {
  border: 1px transparent;
  border-radius: 2px;
  font-size: 12px;
  padding: 3px;
}
</style>
