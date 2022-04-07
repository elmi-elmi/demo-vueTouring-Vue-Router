<template>
  <div v-if="event">
    <h1>{{ event.title }}</h1>
    <router-link :to="{ name: 'EventDetails' }">Details</router-link>
    <router-link :to="{ name: 'EventRegister' }">Register</router-link>
    <router-link :to="{ name: 'EventEdit' }">Edit</router-link>

    <router-view :event="event" />
  </div>
</template>

<script>
import EventService from "@/services/EventService";

export default {
  name: "layout",
  props: ["id"],
  data() {
    return {
      event: null
    };
  },
  created() {
    EventService.getEvent(this.id)
      .then(response => {
        this.event = response.data;
      })
      .catch(error => {
        console.log(error);
      });
  }
};
</script>

<style scoped></style>
