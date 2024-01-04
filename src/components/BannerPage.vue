
<template>
    <div class="container mt-10 mb-10">
        <swiper
            :style="{
                '--swiper-navigation-color': '#fff',
                '--swiper-pagination-color': '#fff',
            }"
            :pagination="{
                type: 'progressbar',
            }" 
            @swiper="onSwiper"
            :navigation="true" 
            :modules="modules" class="swiper" >
            <swiper-slide class="border slide-1">

                <div class="lg:w-1/2">
                    <img class="" src="../assets/images/her.png" alt="">
                </div>
                <div class="lg:w-1/2">
                    <div class="w-full h-full">
                        <div class="text-[#fd3da7] text-4xl mb-1">
                            <p class="title-product">For <span class="sub-title-product">Her</span></p>
                        </div>
                        <div class="lg:p-6">
                            <p class="text-gray-400 lg:text-base sm:text-xs">
                                Whether you're finding an extra special gift for a loved one or trying to find a gift for
                                the hard to buy for mother-in-law our carefully curated gift range caters to all the
                                wonderful women in your life.
                            </p>
                        </div>
                    </div>
                </div>

            </swiper-slide>
            <swiper-slide class="border slide-2">

                <div class="lg:w-1/2">
                    <img class="" src="../assets/images/him.png" alt="">
                </div>
                <div class="lg:w-1/2">
                    <div class="w-full h-full">
                        <div class="text-[#94b198] text-4xl mb-1">
                            <p class="title-product">For <span class="sub-title-product">Him</span></p>
                        </div>
                        <div class="lg:p-6">
                            <p class="text-gray-400 lg:text-base sm:text-xs">
                                Our top selects for your favourite men. We are talking indoor boule for your brother,
                                personalised corkscrew for your dad and hip flask for grandad.
                            </p>
                        </div>
                    </div>
                </div>


            </swiper-slide>
            <swiper-slide>
                <swiper-slide class="border slide-3">

                    <div class="lg:w-1/2">
                        <img class="" src="../assets/images/kids.png" alt="">
                    </div>
                    <div class="lg:w-1/2">
                        <div class="w-full h-full">
                            <div class="text-[#8fbfc4] text-4xl mb-1">
                                <p class="title-product">For <span class="sub-title-product">Kids</span></p>
                            </div>
                            <div class="lg:p-6">
                                <p class="text-gray-400 lg:text-base sm:text-xs">
                                    Our top selects for your favourite men. We are talking indoor boule for your brother,
                                    personalised corkscrew for your dad and hip flask for grandad.
                                </p>
                            </div>
                        </div>
                    </div>

                </swiper-slide>
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import required modules
import { Pagination, Navigation } from 'swiper/modules';
import { ref } from 'vue';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const swiper =  ref(null)
        const onSwiper = (swiper) => {
            swiper.value = swiper
        }

        const handleSlideTo = () => {
           console.log(swiper);
        }
        return {
            modules: [Pagination, Navigation],
            swiper,
            onSwiper,
            handleSlideTo
        };
    },
};
</script>
<style scoped>
.swiper {
    width: 100%;
    height: 300px;
}

.slide-1 {
    background: #fee7ff;
    /* Set the background color for Slide 1 */
}

.slide-2 {
    background: #94b198;
    /* Set the background color for Slide 2 */
}

.slide-3 {
    background: #8fbfc4;
    /* Set the background color for Slide 3 */
}

.swiper-slide {
    text-align: center;
    font-size: 18px;

    /* Center slide content vertically */
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

/* Additional styling for text content inside the slide */
.title-product {
    color: #fff;
    /* Set the text color */
}

.sub-title-product {
    color: #fff;
    /* Set the text color */
}
</style>