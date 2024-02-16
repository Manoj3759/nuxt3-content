<template>
  <div>
    {{ pageData[0] }}
  </div>
  <div>
    <img
      :src="`images/${pageData[0].sectionOnlineProgram.image}`"
      :alt="pageData[0].sectionOnlineProgram.altText"
      width="200px"
      height="200px"
    />
    <h1>title----{{ pageData[0].sectionOnlineProgram.title }}</h1>
    <p>text------{{ pageData[0].sectionOnlineProgram.text }}</p>
    <div
      v-for="(fact, index) in pageData[0].sectionOnlineProgram.facts"
      :key="index"
    >
      <h1>array title--------{{ fact.title }}</h1>
      <p>array text----------{{ fact.text }}</p>
    </div>
  </div>
</template>

<script setup>
let pageData = await queryContent("home").find();
</script>

<style lang="sass" scoped></style>
