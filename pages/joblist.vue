<template>
  <div class="position-relative">
    <TheSearch :filteredJoblist="filteredJoblist" />
    <div class="container">
      <div class="row">
        <div class="col">
          <SearchResult :jobListNumber="filteredData.length" />
        </div>
      </div>
      <div class="row">
        <div class="col-md-2">
          <TheFilter />
        </div>
        <div class="col-md-7">
          <JobList :data="filteredData" />
        </div>
        <div class="col-md-3">
          <Banner />
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import jobListRes from "~/static/joblistData.json";

export default {
  name: "IndexPage",
  data() {
    return {
      data: jobListRes,
      filteredData: jobListRes.result.items
    };
  },
  methods: {
    filteredJoblist(key, value) {
      const searchValue = value.toLowerCase();
      const searchKey = key;
      return this.filteredData = this.data.result.items.filter(item => item?.[searchKey]?.toLowerCase().includes(searchValue) || item.companyName.toLowerCase().includes(searchValue));
    }
  }
};
</script>
