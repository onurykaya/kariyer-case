<template>
  <div class="position-relative no-gutters">
    <div class="container">
      <SupNav />
      <div class="row">
        <div class="col-8 no-gutters">
          <JobInfo :data="data" />
        </div>
        <div class="col-4 no-gutters">
          <DetailBanner :data="data" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import jobDetailRes from "~/static/joblistDetailData.json";

export default {
  name: "id",
  data() {
    return {
      data: {}
    };
  },
  mounted() {
    this.id = Number(this.$route.params.id);
    this.data = jobDetailRes.result.items.find(item => item.jobId === this.id);
  }
};
</script>

<style scoped>
.no-gutters {
  margin-right: -15px !important;
  margin-left: -15px !important;
}
</style>
