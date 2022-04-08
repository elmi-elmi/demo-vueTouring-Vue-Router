<template>
  <div>
    <p>Register section</p>
    <button @click="register">Register</button>
  </div>
</template>

<script>
export default {
  name: "Register",
  props: ["event"],
  inject: ["Gstore"],
  methods: {
    register() {
      this.Gstore.flashmessage =
        "You are successfully register" + this.event.title;
      setTimeout(() => {
        this.Gstore.flashmessage = "";
      }, 2000);
      this.$router.replace({ name: "EventDetails" });
      // this.$router.go(-1);
    }
  }
};
</script>

<style scoped></style>
