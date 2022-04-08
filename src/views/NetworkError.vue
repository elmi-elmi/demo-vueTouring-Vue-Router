<template>
  <div class="networkError">
    <h1>uh-oh!</h1>
    <h3>Network Issues.....</h3>
    <a href="#" @click="$router.go(-1)">go back</a>
  </div>
</template>

<script>
export default {
  name: "NetworkError"
};
</script>

<style scoped></style>
