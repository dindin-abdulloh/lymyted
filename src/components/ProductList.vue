<!-- <template>
    <div class="container">
        <div class="flex flex-wrap gap-6 container">
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/5 px-2 mb-4 border py-3 rounded-lg">
                <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                    <img
                        src="https://tecdn.b-cdn.net/img/new/fluid/city/113.webp"
                        class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                        alt="Louvre" />
                </div>
                <div class="mt-3">
                    <a href="#">
                       <div>
                            <p class="product-name text-xl">Leather Cosmetics Case</p>
                       </div>
                       <div class="mt-2">
                <p class="product-name text-lg relative overflow-hidden">
                    Rp 1.300.000,00 IDR
                    <span class="underline"></span>
                </p>
            </div>
                    </a>
                </div>
            </div>
            

            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/5 px-2 mb-4 border py-3 rounded-lg">
                <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                    <img
                        src="https://tecdn.b-cdn.net/img/new/fluid/city/113.webp"
                        class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                        alt="Louvre" />
                </div>
                <div class="mt-3">
                    <a href="#">
                       <div>
                            <p class="product-name text-xl">Leather Cosmetics Case</p>
                       </div>
                       <div class="mt-2">
                <p class="product-name text-lg relative overflow-hidden">
                    Rp 1.300.000,00 IDR
                    <span class="underline"></span>
                </p>
            </div>
                    </a>
                </div>
            </div>

            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/5 px-2 mb-4 border py-3 rounded-lg">
                <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                    <img
                        src="https://tecdn.b-cdn.net/img/new/fluid/city/113.webp"
                        class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                        alt="Louvre" />
                </div>
                <div class="mt-3">
                    <a href="#">
                       <div>
                            <p class="product-name text-xl">Leather Cosmetics Case</p>
                       </div>
                       <div class="mt-2">
                <p class="product-name text-lg relative overflow-hidden">
                    Rp 1.300.000,00 IDR
                    <span class="underline"></span>
                </p>
            </div>
                    </a>
                </div>
            </div>

            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/5 px-2 mb-4 border py-3 rounded-lg">
                <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                    <img
                        src="https://tecdn.b-cdn.net/img/new/fluid/city/113.webp"
                        class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                        alt="Louvre" />
                </div>
                <div class="mt-3">
                    <a href="#">
                       <div>
                            <p class="product-name text-xl">Leather Cosmetics Case</p>
                       </div>
                       <div class="mt-2">
                <p class="product-name text-lg relative overflow-hidden">
                    Rp 1.300.000,00 IDR
                    <span class="underline"></span>
                </p>
            </div>
                    </a>
                </div>
            </div>
            
            <div class="w-full sm:w-1/2 md:w-1/3 lg:w-1/5 px-2 mb-4 border py-3 rounded-lg">
                <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                    <img
                        src="https://tecdn.b-cdn.net/img/new/fluid/city/113.webp"
                        class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                        alt="Louvre" />
                </div>
                <div class="mt-3">
                    <a href="#">
                       <div>
                            <p class="product-name text-xl">Leather Cosmetics Case</p>
                       </div>
                       <div class="mt-2">
                <p class="product-name text-lg relative overflow-hidden">
                    Rp 1.300.000,00 IDR
                    <span class="underline"></span>
                </p>
            </div>
                    </a>
                </div>
            </div>

           
        </div>
    </div>
</template> -->

<!-- <style scoped>
.relative {
    position: relative;
}

.underline {
    position: absolute;
    left: 0;
    bottom: 0;
    width: 0;
    height: 2px;
    background-color: #3490dc; /* Change the color to your desired underline color */
    transition: width 0.3s ease-in-out;
}

.product-name:hover .underline {
    width: 100%;
}
</style> -->

<template>
    <div class="container">
        <swiper :breakpoints="breakpoints" :modules="modules" :a11y="true" :centeredSlides="true" :spaceBetween="20"  :navigation="true" :virtual="true" class="mySwiper" @swiper="setSwiperRef">
            <swiper-slide v-for="(slideContent, index) in slides" :key="index" :virtualIndex="index" class="border rounded-lg">
                    <div class="relative max-w-xs overflow-hidden bg-cover bg-no-repeat rounded-md">
                        <img :src="slideContent.imageSrc"
                            class="max-w-xs transition duration-300 ease-in-out hover:scale-110"
                            :alt="slideContent.altText" />
                    </div>
                    <div class="mt-3 p-2">
                        <a :href="slideContent.link">
                            <div>
                                <p class="product-name text-md">{{ slideContent.productName }}</p>
                            </div>
                            <div class="mt-2">
                                <p class="product-name text-md relative overflow-hidden">
                                    {{ slideContent.price }}
                                    <span class="underline"></span>
                                </p>
                            </div>
                        </a>
                    </div>
            </swiper-slide>
        </swiper>
        <!-- <p class="append-buttons">
          
            <button @click="slideTo(1)" class="prepend-slide">Slide 1</button>
            <button @click="slideTo(250)" class="slide-250">Slide 250</button>
            <button @click="slideTo(500)" class="slide-500">Slide 500</button>
            <button @click="append()" class="append-slides">Append Slide</button>
        </p> -->
    </div>
</template>
<script>
import { ref } from 'vue';
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';
import 'swiper/css/virtual';

// import './style.css';

// import Swiper core and required modules
import { Pagination, Navigation, Virtual } from 'swiper/modules';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        // Create array with 500 slides
        // const slides = ref(
        //   Array.from({ length: 500 }).map((_, index) => `Slide ${index + 1}`)
        // );
        let swiperRef = null;
        let appendNumber = 500;
        let prependNumber = 1;

        const slides = [
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            {
                imageSrc: 'https://tecdn.b-cdn.net/img/new/fluid/city/113.webp',
                altText: 'Louvre',
                link: '#',
                productName: 'Leather Cosmetics Case',
                price: 'Rp 1.300.000,00 IDR',
            },
            // Add more slides as needed
        ]

       const  breakpoints = {
        475: {
          slidesPerView: 1,
          spaceBetween: 0,
        
        },
        640: {
          slidesPerView: 2,
          spaceBetween: 20,
        },
        768: {
          slidesPerView: 5,
          spaceBetween: 40,
        },
        1024: {
          slidesPerView: 5,
          spaceBetween: 20,
        },
      }

        const setSwiperRef = (swiper) => {
            swiperRef = swiper;
        };
        const slideTo = (index) => {
            swiperRef.slideTo(index - 1, 0);
        };
        const append = () => {
            slides.value = [...slides.value, 'Slide ' + ++appendNumber];
        };
        const prepend = () => {
            slides.value = [
                `Slide ${prependNumber - 2}`,
                `Slide ${prependNumber - 1}`,
                ...slides.value,
            ];
            prependNumber -= 2;
            swiperRef.slideTo(swiperRef.activeIndex + 2, 0);
        
     
        };
        return {
            slides,
            swiperRef: null,
            appendNumber,
            prependNumber,
            setSwiperRef,
            slideTo,
            append,
            prepend,
            modules: [Pagination, Navigation, Virtual],
            breakpoints
        };
    },
};
</script>

<style scoped>
body {
    background: #eee;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 14px;
    color: #000;
    margin: 0;
    padding: 0;
}

.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: flex;
    justify-content: center;
    align-items: center;
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.swiper {
    width: 100%;
    /* height: 300px; */
    margin: 20px auto;
}

.append-buttons {
    text-align: center;
    margin-top: 20px;
}

.append-buttons button {
    display: inline-block;
    cursor: pointer;
    border: 1px solid #007aff;
    color: #007aff;
    text-decoration: none;
    padding: 4px 10px;
    border-radius: 4px;
    margin: 0 10px;
    font-size: 13px;
}

</style>
  