
<template>
    <section class="mb-[30px] block section-slider">
        <div class="xl:max-w-[1230px] px-[15px] m-auto">
        <Swiper 
        :modules="[EffectFade, Navigation, Pagination]" 
        :effect="'fade'"
        :loop="true"
        :autoplay="{
            delay: 300,
            disableOnInteraction: false,
        }"
        :spaceBetween="30"
        :navigation="true"
        :pagination="{
            clickable: true,
        }"
        
    >
        <SwiperSlide v-for="slide in slides">
            <img :src="`/slide/${slide}`" alt="">
        </SwiperSlide>
    </Swiper>
    </div>
    </section>
    <section class="mb-[30px] block section-policies">
        <div class="overflow-hidden">
            <div class="m-auto xl:max-w-[1230px] px-[15px]">
                <div class="m-auto flex justify-between gap-[15px] overflow-auto">
                    <div class="text-[14px] p-[10px] grid gap-[15px] bg-white text-[#050000]" style="flex-basis: calc(25% - 15px); grid-template-columns: 40px 1fr;">
                        <div><img src="/policies/policies_icon_1.webp" alt="" width="40" height="40"></div>
                        <div>
                            <h3 class="text-[16px] font-semibold leading-tight mb-[5px]">Miễn phí vận chuyển</h3>
                            <div class="opacity-75">Nhận hàng trong vòng 3 ngày</div>
                        </div>
                    </div>
                    <div class="text-[14px] p-[10px] grid gap-[15px] bg-white text-[#050000]" style="flex-basis: calc(25% - 15px); grid-template-columns: 40px 1fr;">
                        <div><img src="/policies/policies_icon_2.webp" alt="" width="40" height="40"></div>
                        <div>
                            <h3 class="text-[16px] font-semibold leading-tight mb-[5px]">Quà tặng hấp dẫn</h3>
                            <div class="opacity-75">Nhiều ưu đãi khuyến mãi hot</div>
                        </div>
                    </div>
                    <div class="text-[14px] p-[10px] grid gap-[15px] bg-white text-[#050000]" style="flex-basis: calc(25% - 15px); grid-template-columns: 40px 1fr;">
                        <div><img src="/policies/policies_icon_3.webp" alt="" width="40" height="40"></div>
                        <div>
                            <h3 class="text-[16px] font-semibold leading-tight mb-[5px]">Bảo đảm chất lượng</h3>
                            <div class="opacity-75">Sản phẩm đã dược kiểm định</div>
                        </div>
                    </div>
                    <div class="text-[14px] p-[10px] grid gap-[15px] bg-white text-[#050000]" style="flex-basis: calc(25% - 15px); grid-template-columns: 40px 1fr;">
                        <div><img src="/policies/policies_icon_4.webp" alt="" width="40" height="40"></div>
                        <div>
                            <h3 class="text-[16px] font-semibold leading-tight mb-[5px]">Hotline: 19001993</h3>
                            <div class="opacity-75">Dịch vụ hỗ trợ bạn 24/7</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="mb-[30px] block section-season_coll">
        <section class="mb-[30px] block">
            <div class="m-auto xl:max-w-[1230px] rounded-[8px] p-[15px]">
                <h2 class="text-[#333] text-[2rem] m-0 leading-tight text-center font-normal">Thời trang EGA</h2>
                <div class="xl:mx-[-15px]">
                    <div class="relative block mx-0 overflow-x-auto overflow-y-hidden text-center">
                        <div class="p-0 m-0 ">
                            <Swiper 
                            :slidesPerView="6"
                            :spaceBetween="10"
                            :breakpoints="{
                                '640': {
                                    slidesPerView: 2,
                                    spaceBetween: 20,
                                },
                                '768': {
                                    slidesPerView: 4,
                                    spaceBetween: 40,
                                },
                                '1024': {
                                    slidesPerView: 6,
                                    spaceBetween: 30,
                                },
                            }"
                            >   
                            <SwiperSlide v-for="ss in seasons">
                                <div class="relative py-[30px] px-[15px] ss_item">
                                    <a href="/" class="block">
                                        <div class="">
                                            <img :src="`/season/${ss.photo}`" alt="" width="200" height="200">
                                        </div>
                                        <div class="grid grid-cols-1 items-center relative p-0 left-auto bottom-auto mt-[10px]">
                                            <div class="text-center text-[18px] font-semibold">{{ ss.name }}</div>
                                            <span class="text-center text-[14px] text-[#888]">{{ ss.number }} sản phẩm</span>
                                        </div>
                                    </a>
                                </div>
                            </SwiperSlide>
                            </Swiper>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </section>
    <section class="mb-[30px] block section-coupons">
        <div>
            <div class="m-auto px-[15px] xl:max-w-[1230px]">
                <div class="flex xl:justify-center flex-wrap mx-[-0.5rem]">
                    <div class="py-[5px] px-[15px] flex xl:basis-1/4 xl:max-w-[25%] lg:basis-1/2 lg:max-w-[50%] md:basis-5/12" v-for="coupon in coupons">
                        <div class="relative bg-white flex min-h-[100px] h-full drop-shadow-lg">
                            <div class="relative block w-20 py-2 pl-2 pr-1 bg-white basis-20 ">
                                <img :src="`/coupons/${coupon.photo}`" :alt="`${coupon.photo}`" width="79" height="70" class="absolute object-contain w-auto h-auto top-1/2 left-1/2" style="max-width: calc(100% - 12px); transform: translate(-50%, -50%) scale(1);">
                            </div>
                            <div class="flex flex-col justify-between py-[12px] max-w-[194px] px-[15px]">
                                <div class="text-center">
                                    <h3 class="text-base leading-[1.2] text-[--coupon-title-color] font-semibold mb-[10px]">NHẬP MÃ: {{ coupon.id }}</h3>
                                    <div class="text-sm leading-[1.2] text-[#727272] pb-5">{{ coupon.desc }}</div>
                                </div>
                                <div class="flex flex-wrap items-center justify-between">
                                    <button class="border-none pt-[2px] pb-[3px] px-2 rounded-none mb-[3px] bg-[--coupon-button-color] text-white text-sm leading-[1.5] font-normal text-center">
                                        <span class="block h-6 text-[14px] leading-6">Sao chép</span>
                                    </button>
                                    <span class="text-[14px] text-[#353945] cursor-pointer mb-[3px] underline ml-[10px]">Điều kiện</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="mb-[30px] block section-flashsale">
        <div class="px-[15px] xl:max-w-[1230px] m-auto">
            <div class="rounded-[10px] bg-white p-0 border-[0]">
                <div class="bg-transparent mb-[5px] flex flex-wrap lg:text-base py-0 items-center justify-between">
                    <div class="flex flex-wrap items-center justify-between max-w-full basis-full">
                        <div class="flash-sale-heading">
                            <div class="flex items-center gap-[10px]">
                                <h2 class="text-black text-[2em] leading-[1.2] text-center font-normal m-0"> <a href="/" class="font-bold text-black cursor-pointer" title="GIẢM SỐC 50%">GIẢM SỐC 50%</a></h2>
                                <img class="max-h-[55px] max-w-full" src="/flashsale-hot.png" alt="" width="50" height="50">
                            </div>
                        </div>
                        <div class="pt-0 flex justify-center items-center flex-wrap ml-[15px]">
                            <span class="static font-normal block text-[#155BF6] text-[16px] mr-2">Kết thúc sau</span>
                            <div>
                                <div class="flex items-center gap-2">
                                    <div class="flex flex-col bg-black rounded-md">
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.hours > 10">{{ timing.hours % 24}}</div>
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.hours < 10">0{{ timing.hours % 24}}</div>
                                        <span class="text-center text-[10px] py-0 text-white">Giờ</span>
                                    </div>
                                    <div class="flex flex-col bg-black rounded-md">
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.minutes > 10">{{ timing.minutes % 60}}</div>
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.minutes < 10">0{{ timing.minutes % 60}}</div>
                                        <span class="text-center text-[10px] py-0 text-white">Phút</span>
                                    </div>
                                    <div class="flex flex-col bg-black rounded-md">
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.seconds > 10">{{ timing.seconds % 60}}</div>
                                        <div class="text-[25px] p-[10px] border-b border-slate-600 text-white" v-if="timing.seconds < 10">0{{ timing.seconds % 60}}</div>
                                        <span class="text-center text-[10px] py-0 text-white">Giây</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <TabsWrapper>
                                <Tab title="Tab 1">Hello from Tab 1</Tab>
                                <Tab title="Tab 2">Hello from Tab 2</Tab>
                                <Tab title="Tab 3">Hello from Tab 3</Tab>
                                <Tab title="Tab 4">Hello from Tab 4</Tab>
                            </TabsWrapper>
                </div>
            </div>
        </div>
    </section>
    <section>Tạo mới</section>
</template>
<style>

/* Carousel Slide START */
.swiper-button-next,
.swiper-button-prev {
    padding: 20px;
    width: calc(var(--swiper-navigation-size) / 44 * 27);
    height: var(--swiper-navigation-size);
    font-weight: bold;
    color: #767676;
    background-color: #ebebeb;
    border-radius: 100%;
    opacity: 0.7 !important;
    z-index: 1;
    transition: all 0.3s ease;
}

.swiper-button-next:not(.swiper-button-disabled):hover,
.swiper-button-prev:hover {
    opacity: 1;
    box-shadow: 1px 2px 10px rgba(0, 0, 0, 0.4);
    background: #fff !important;
    color: #333;
}

.swiper-pagination-bullet {
    height: 4px;
    width: 16px;
    border: 1px solid #fff;
    border-radius: 2px !important;
    background: #fff;
    border-radius: 0;
    margin: 0 3px;
    opacity: .5;
    margin: 0 2px !important;
}

.swiper-pagination-bullet-active {
    opacity: 1;
    border-color: #333;
    background-color: #000;
}

/* Carousel Slide END */

.ss_item {
    transition: transform 0.64s cubic-bezier(0.15, 0.75, 0.5, 1) 0s;
}

.ss_item:hover {
    transform: scale(1.08) translateZ(0);
}


</style>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { EffectFade, Navigation, Pagination } from 'swiper/modules';
// import { Tab, TabsWrapper } from "./components"; 

// // Import Swiper Style
import "swiper/css";
import 'swiper/css/effect-fade';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

const slides = ['slider_1.jpg', 'slider_2.webp'];

const seasons = [
    {
        photo: 'season_coll_1_img_medium.webp', name: 'Áo khoác', number: 8
    },
    {
        photo: 'season_coll_2_img_large.png', name: 'Áo sơ mi', number: 6
    },
    {
        photo: 'season_coll_3_img_large.webp', name: 'Áo thun', number: 7
    },
    {
        photo: 'season_coll_4_img_large.webp', name: 'Quần dài nam', number: 5
    },
    {
        photo: 'season_coll_5_img_large.webp', name: 'Quần Jeans', number: 4
    },
    {
        photo: 'season_coll_6_img_large.webp', name: 'Quần Short', number: 6
    },
];

const coupons = [ 
    {   photo: 'coupon_1_img.webp', id: 'EGA10', desc: 'Mã giảm 10% cho đơn hàng tối thiểu 1.5 triệu', condition: ['Mã giảm 10% cho đơn hàng có giá trị tối thiểu 1.5 triệu', 'Giảm tối đa 500k']   },
    {   photo: 'coupon_2_img.webp', id: 'EGA15', desc: 'Mã giảm 15% cho đơn hàng tối thiểu 2 triệu', condition: ['Mã giảm 15% cho đơn hàng có giá trị tối thiểu 2 triệu', 'Giảm tối đa 500k']   },
    {   photo: 'coupon_3_img.webp', id: 'EGA99', desc: 'Giảm giá 99k các sản phẩm Áo thun', condition: ['Giảm giá 99k các sản phẩm Áo thun', 'Tổng giá trị sản phẩm từ 1 triệu trở lên']   },
    {   photo: 'coupon_4_img.webp', id: 'EGAFREESHIP', desc: 'Miễn phí ship cho đơn hàng tối thiểu 500.000đ', condition: ['Miễn phí ship 100K cho đơn hàng tối thiểu từ 500.000đ', 'Áp dụng cho tất cả tỉnh / thành phố']   },
];

const timing = {    hours: 0, minutes: 0, seconds: 0     };
const launchDate = new Date('28 October 2023');

function runCountDown() {
    setInterval(() => {
        const currDate = new Date();
        const launchTime = launchDate - currDate;

        timing.seconds = parseInt(launchTime / 1000);
        timing.minutes = parseInt(launchTime / 60);
        timing.hours = parseInt(launchTime / 60);
    }, 1000);
}

// runCountDown();

</script>
