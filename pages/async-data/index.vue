<template>
  <div>
    ------------
    {{ pageData.data }}
  </div>
</template>

<script setup>
const pageData = await useAsyncData("home", () =>
  queryContent("home").findOne()
);
</script>

<style lang="sass" scoped></style>
