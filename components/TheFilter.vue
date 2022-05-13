<template>
  <div class="wrapper shadow no-gutters mt-4">
    Left Filter Component
  </div>
</template>

<script>
export default {
  name: "TheFilter"
};
</script>

<style scoped>
.wrapper {
  align-items: center;
  display: flex;
  justify-content: center;
  height: 100%;
  width: 100%;
}

.shadow {
  background-color: white;
  border-radius: 4px;
  box-shadow: 0 1px 2px 0 rgb(0 0 0 / 10%);
  padding: 1rem;
  text-align: center;
}
</style>
