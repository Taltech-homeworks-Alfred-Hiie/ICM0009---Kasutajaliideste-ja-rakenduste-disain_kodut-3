<template>
  <h1 class="centered-title">
    <slot></slot>
  </h1>
</template>

<style scoped>
.centered-title {
  text-align: center;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 2.5em;
  color: #333;
  margin-top: 20px;
  margin-bottom: 10px;
}
</style>
