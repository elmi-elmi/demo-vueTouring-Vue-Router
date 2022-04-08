<template>
  <div>
    <h1>Oops!</h1>
    <h3>The {{ resource }} does not found.</h3>
    <router-link :to="{ name: 'EventList' }">Back to home</router-link>
  </div>
</template>

<script>
export default {
  name: "NotFound",
  props: {
    resource: {
      type: String,
      required: true,
      default: "page"
    }
  }
};
</script>

<style scoped></style>
