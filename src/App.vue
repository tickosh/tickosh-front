<script setup lang="ts">
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
import EventCard from "@/components/EventCard.vue";

import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
</script>

<template>
  <div class="flex flex-col h-full">
    <Navbar />
    <section class="flex-grow">
      <div class="p-6">
        <swiper
          :breakpoints="{
            320: {
              slidesPerView: 1,
              spaceBetween: 10,
            },
            640: {
              slidesPerView: 2,
              spaceBetween: 12,
            },
            768: {
              slidesPerView: 4,
              spaceBetween: 14,
            },
            1280: {
              slidesPerView: 6,
              spaceBetween: 16,
            },
          }"
        >
          <swiper-slide v-for="i in 7" :key="i">
            <EventCard
              :id="1"
              title="Inception"
              poster="https://image.tmdb.org/t/p/w500/9gk7adHYeDvHkCSEqAvQNLV5Uge.jpg"
              location="Almaty Arena"
              :price="13000"
              :timestamp="new Date('2022-05-16')"
            />
          </swiper-slide>
        </swiper>
      </div>
    </section>
    <Footer />
  </div>
</template>

<style scoped></style>
