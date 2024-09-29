

<template>
  <div class="shadow-xl transition-all hover:shadow-primary">
    <div class="rounded-t-xl overflow-hidden relative group">
      <img
        v-if="imgUrl.length === 1 && typeof imgUrl[0] === 'string'"
        :src="imgUrl[0]"
        alt="Project Image"
        class="w-full h-full object-cover"
      />

      <div v-else>
<swiper     :slidesPerView="1"
    :spaceBetween="30"
    :loop="true"
    :pagination="{
      clickable: true,
    }"
    :navigation="true"
    :modules="modules" class="mySwiper">



    <swiper-slide v-for="(img, index) in imgUrl" :key="index">
      <img v-if="typeof img === 'string'" :src="img" alt="Project Image" class="d-block w-100" />
    </swiper-slide>

  </swiper>
        <!-- <swiper
      :slides-per-view="1"
      space-between="30"
      navigation
      pagination
      loop
      class="mySwiper"
    >
      Loop through the imgUrl array and display each image
      <swiper-slide v-for="(img, index) in imgUrl" :key="index">
        <img 
          v-if="typeof img === 'string'" 
          :src="img" 
          alt="Project Image" 
          class="w-full h-full object-cover"
        />
      </swiper-slide>
    </swiper> -->
      </div>
    </div>
    <div class="rounded-b-xl mt-1 py-3 md:!py-6 px-2 md:!px-6">
      <p class="dark:text-[#ADB7BE] text-slate-800" v-html="description"></p>
      <p v-html="description"></p>
    </div>
  </div>
</template>
<script setup>
// Import Swiper components
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
// Import required modules
import { Navigation } from 'swiper/modules';

const modules = [Navigation];
const props = defineProps({
  description: { type: String, required: true },
  imgUrl: { type: Array, required: true },
});
</script>