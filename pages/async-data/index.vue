<template>
  <div>
    ------------
    {{ pageData.data }}
    <div>
      <h1>title----{{ pageData[0].sectionOnlineProgram.title }}</h1>
      <p>text------{{ pageData[0].sectionOnlineProgram.text }}</p>
    </div>
  </div>
</template>

<script setup>
const pageData = await useAsyncData("home", () =>
  queryContent("home").findOne()
);
</script>

<style lang="sass" scoped></style>
