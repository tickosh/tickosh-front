<script lang="ts" setup>
import { defineProps } from "vue";
import type { Event } from "@/types";

import moment from "moment";

import IconCalendar from "./icons/IconCalendar.vue";
import IconPin from "./icons/IconPin.vue";
import IconCash from "./icons/IconCash.vue";

const props = defineProps<Event>();
</script>
<template>
  <div class="flex flex-col justify-center">
    <img
      :src="props.poster"
      alt="Event poster"
      class="w-48 h-72 object-cover rounded-xl mb-3"
    />
    <h2 class="text-base font-bold mb-3">{{ props.title }}</h2>
    <p
      class="text-sm flex items-center text-gray-500 mb-3 gap-x-3 font-semibold"
    >
      <IconCalendar class="w-5 h-5 mx-1" />
      {{ moment(props.timestamp).format("ddd DD MMM, HH:mm") }}
    </p>
    <p
      class="text-sm flex items-center text-gray-500 mb-3 gap-x-3 font-semibold"
    >
      <IconPin class="w-5 h-5 mx-1" />
      {{ props.location }}
    </p>
    <p
      class="text-sm flex items-center text-gray-500 mb-3 gap-x-3 font-semibold"
    >
      <IconCash class="w-5 h-5 mx-1" />
      from {{ props.price }} ₸
    </p>
  </div>
</template>
