<template>
  <div>
    <SupNav />
    <div class="row">
      <div class="col-12 mt-4">
      <span class="result">
        {{ jobListNumber }}
      </span>
        <span class="result">
         İş İlanları
      </span>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "SearchResult",
  props: ["jobListNumber"]
};
</script>

<style scoped>
.result {
  font-size: 1.2rem;
}
</style>
