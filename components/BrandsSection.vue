<template>
    <div class="py-20 bg-[#F8FAFC]">
  <div id="Brands" >
    <div class="flex justify-center mb-8">
        <h2 class="text-black font-bold text-xl lg:text-5xl">Brands I Have Worked With:</h2>
    </div>
    <Swiper
      :slides-per-view="6"
        space-between="0"
        :breakpoints="{
          320: {
            slidesPerView: 2,
            spaceBetween: 10,
          },
          768: {
            slidesPerView: 4,
            spaceBetween: 0,
          },
          1024: {
            slidesPerView: 6,
            spaceBetween: 0,
          },
        }"
        class="mySwiper max-w-[1200px] w-full px-3 md:px-0"
        loop="true"

    >
      <SwiperSlide v-for="(client, index) in clients" :key="index" clas>
        <img :src="client" alt="Client Logo" class="border-[2.5px] border-primary  rounded-full w-40 h-36 md:h-40" />
      </SwiperSlide>
    </Swiper>
  </div>
  <div id="Tools" class="px-2 md:!px-10 lg:!px-40 mt-20 pt-20 ">
    <div class="flex justify-center md:justify-start">
        <h2 class="text-center md:!text-start text-black font-extrabold !text-xl md:!text-3xl lg:!text-5xl">TOOLS WORK ON IT </h2>
    </div>
    <div class="mx-auto grid grid-cols-2 md:grid-cols-3  lg:grid-cols-4 lg:gap-10 xl:grid-cols-5">
        <div v-for="(tool , index) in tools" :key="index" class=" flex justify-center p-4">
            <img :src="tool" class="w-full h-full" alt="">
        </div>
    </div>
  </div></div>
</template>

<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';

const clients = ref([
  "https://i.postimg.cc/bwyyD7Yy/1.png",
  "https://i.postimg.cc/KvcwnxTH/2.png",
  "https://i.postimg.cc/Px33y8YV/3.png",
  "https://i.postimg.cc/pdnz4hw1/4.png",
  "https://i.postimg.cc/JzSBN7s3/5.png",
  "https://i.postimg.cc/W3wFcMXS/6.png",
  "https://i.postimg.cc/c1TgDBKL/7.png",
  // "https://i.postimg.cc/Fz8tMKgz/client-8.png",
  "https://i.postimg.cc/65m7K6fs/8.png",
  "https://i.postimg.cc/L6ws7Cm2/9.png",
  "https://i.postimg.cc/7hKfYHTw/lofo-1.png",
  "https://i.postimg.cc/Z5G0qD0B/logo-2.png",
  "https://i.postimg.cc/9fy0wtqx/logo-3.png",
]);

const tools = ref([
  "https://i.postimg.cc/NGkZRByR/tool-1.jpg",
  "https://i.postimg.cc/wTxZVZJZ/tool-2.png",
  "https://i.postimg.cc/5NPGkgS0/tool-3.jpg",
  "https://i.postimg.cc/fLhg0rDH/tool-4.png",
  "https://i.postimg.cc/pLh0cHdG/tool-5.png",
  "https://i.postimg.cc/DwksFkgY/tool-6.png",
  "https://i.postimg.cc/WpdX1VG2/tool-10.png",
  "https://i.postimg.cc/66Fz7PcC/tool-7.png",
  "https://i.postimg.cc/kgmcstk4/tool-8.png",
  "https://i.postimg.cc/c4Yhfck2/tool-9.png",
  "https://i.postimg.cc/W45qdnKB/tool-11.png"
]);
</script>

<style scoped>
.mySwiper {
  width: 100%;
  height: 100%;
}
</style>
