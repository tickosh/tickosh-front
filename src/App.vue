<script setup lang="ts">
import EventCard from "@/components/EventCard.vue";
</script>

<template>
  <div class="flex flex-row gap-4 p-2">
    <EventCard
      :id="1"
      title="Inception"
      poster="https://image.tmdb.org/t/p/w500/9gk7adHYeDvHkCSEqAvQNLV5Uge.jpg"
      location="Almaty Arena"
      :price="13000"
      :timestamp="new Date('2022-05-16')"
    />
    <EventCard
      :id="1"
      title="Inception"
      poster="https://image.tmdb.org/t/p/w500/9gk7adHYeDvHkCSEqAvQNLV5Uge.jpg"
      location="Almaty Arena"
      :price="13000"
      :timestamp="new Date('2022-05-16')"
    />
    <EventCard
      :id="1"
      title="Inception"
      poster="https://image.tmdb.org/t/p/w500/9gk7adHYeDvHkCSEqAvQNLV5Uge.jpg"
      location="Almaty Arena"
      :price="13000"
      :timestamp="new Date('2022-05-16')"
    />
    <EventCard
      :id="1"
      title="Inception"
      poster="https://image.tmdb.org/t/p/w500/9gk7adHYeDvHkCSEqAvQNLV5Uge.jpg"
      location="Almaty Arena"
      :price="13000"
      :timestamp="new Date('2022-05-16')"
    />
  </div>
</template>

<style scoped></style>
