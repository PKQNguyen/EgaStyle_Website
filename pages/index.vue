
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
                    <TabsWrapper class="tab-flashsale">
                                <Tab title="Hàng hiệu -50%">
                                    <div>
                                        <Swiper :watchSlidesProgress="true" :slidesPerView="5">
                                            <SwiperSlide v-for="pro in products" :key="pro.id" class="px-[15px] flex xl:basis-1/5 xl:max-w-[20%]">
                                                <div class="flex" v-if="pro.cate === 'T-Shirt'">
                                                    <div class="item_product rounded-lg h-full flex flex-col justify-between mt-0 mb-2 lg:text-[16px] lg:mb-[30px] bg-white">
                                                        <form action="/">
                                                            <div class="relative overflow-hidden product-thumbnail group">
                                                                <a href="#" 
                                                                    class="relative block w-full p-0 overflow-hidden text-[#000] font-bold 
                                                                            before:content-[''] before:block lg:group-hover:scale-95" 
                                                                    :title="`${pro.name}`" style="transition: transform .3s ease-out;">
                                                                    <img src="/products/frame_2.webp" class="product-frame absolute top-1/2 left-1/2 translate-x-[-50%] translate-y-[-50%] scale-100 object-contain w-auto h-auto max-w-full max-h-full min-w-[1px] min-h-[1px] z-10" alt="">
                                                                    <img :src="`/products/sale_50/${pro.img_thumbnail}`" 
                                                                        class="absolute top-1/2 left-1/2 translate-x-[-50%] translate-y-[-50%] scale-100 
                                                                            object-contain w-auto h-auto max-w-full max-h-full min-w-[1px] min-h-[1px]" 
                                                                        alt="" width="480" height="480"
                                                                    >
                                                                    <img :src="`/products/sale_50/${pro.img_hover}`" 
                                                                        class="absolute top-1/2 left-1/2 translate-x-[-50%] translate-y-[-50%] scale-100 
                                                                            object-contain w-auto h-auto max-w-full max-h-full min-w-[1px] min-h-[1px] 
                                                                            opacity-0 z-[-1] group-hover:opacity-100 group-hover:z-[1]" 
                                                                        alt="" width="480" height="480"
                                                                    >
                                                                </a>
                                                                <input type="hidden" name="id">
                                                                <div class="absolute bottom-[15px] left-1/2 bg-white flex justify-center rounded-[5px] opacity-0 translate-x-[-50%] translate-y-[150%]
                                                                            lg:group-hover:opacity-100 lg:group-hover:z-10 lg:group-hover:translate-x-[-50%] lg:group-hover:translate-y-[0]" 
                                                                    style="box-shadow: 0 5px 10px rgba(0, 0, 0, 0.05); transition: all .3s ease;">
                                                                    <a href="#" 
                                                                        class="bg-white flex items-center justify-center relative border-r border-solid border-r-[#eee] 
                                                                            h-[45px] w-[45px] m-0 p-0 text-[14px] group/btn-view hover:bg-black hover:text-white hover:opacity-100" 
                                                                        style="transition: all .3s ease; border-radius: 5px 0 0 5px;">
                                                                        <Icon name="ion:md-cart" class="text-[20px]"/>
                                                                        <span class="opacity-0 invisible absolute bottom-full left-1/2 bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] translate-x-[-50%] block w-auto min-w-max
                                                                                    group-hover/btn-view:opacity-100 group-hover/btn-view:visible group-hover/btn-view:bottom-[calc(100%+8px)]
                                                                                    before:content-[''] before:bg-transparent before:absolute before:h-2 before:left-0 before:top-full before:w-full
                                                                                    after:content-[''] after:bg-[#333] after:h-[10px] after:absolute after:w-[10px] after:rotate-45 after:left-[calc(50%-5px)] after:bottom-[-5px]"
                                                                            style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
                                                                        >Tùy chọn</span>
                                                                    </a>
                                                                    <a href="#" 
                                                                        class="bg-white flex items-center justify-center relative
                                                                            h-[45px] w-[45px] m-0 p-0 text-[14px] group/btn-view hover:bg-black hover:text-white hover:opacity-100" 
                                                                        style="transition: all .3s ease; border-radius:  0 5px 5px 0;">
                                                                        <Icon name="ion:eye-sharp" class="text-[20px]" />
                                                                        <span class="opacity-0 invisible absolute bottom-full left-1/2 bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] translate-x-[-50%] block w-auto min-w-max
                                                                                    group-hover/btn-view:opacity-100 group-hover/btn-view:visible group-hover/btn-view:bottom-[calc(100%+8px)]
                                                                                    before:content-[''] before:bg-transparent before:absolute before:h-2 before:left-0 before:top-full before:w-full
                                                                                    after:content-[''] after:bg-[#333] after:h-[10px] after:absolute after:w-[10px] after:rotate-45 after:left-[calc(50%-5px)] after:bottom-[-5px]"
                                                                            style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
                                                                        >Xem nhanh</span>
                                                                    </a>
                                                                </div>
                                                                <div class="hidden absolute top-[10px] right-[10px] left-auto text-center bg-[#eee] py-[7px] px-[2px] font-medium z-[3] w-11 h-11 rounded-full text-[14px]">
                                                                    <img src="/products/ega-product-gift.png" class="inline-block max-w-[20px]" width="20" height="20" alt="product gift">
                                                                </div>
                                                            </div>
                                                            <div class="py-[3px] lg:pt-[10px] relative pr-[30px]">
                                                                <span class="text-[12px] uppercase inline-block text-[#969696] tracking-[1.8px]">{{ pro.brand }}</span>
                                                                <button class="appearance-none border-none bg-transparent absolute right-0 top-[10px] z-10 group">
                                                                    <Icon name="ion:heart" style="display: none !important;"></Icon>
                                                                    <Icon name="ion:android-favorite-outline"></Icon>
                                                                    <div class="opacity-0 invisible absolute bottom-full bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] left-1/2 translate-x-[-50%] block w-auto min-w-max
                                                                                group-hover:opacity-100 group-hover:visible group-hover:bottom-[calc(100%+8px)]
                                                                                before:content-[''] before:bg-transparent before:absolute before:h-2 before:left-0 before:top-full before:w-full
                                                                                after:content-[''] after:bg-[#333] after:h-[10px] after:absolute after:rotate-45 after:w-[10px] after:left-[calc(50%-5px)] after:bottom-[-5px]" 
                                                                        style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);">
                                                                        <span class="hidden">Bỏ yêu thích</span>
                                                                        <span>Yêu thích</span>
                                                                    </div>
                                                                </button>
                                                                <div class="product-name overflow-hidden mb-[5px] text-[16px] font-normal leading-[1.4]" 
                                                                    style="display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; white-space: initial;">
                                                                    <a href="#" class="text-[#000] font-medium hover:text-[#2F80ED]" :title="`${pro.name}`">
                                                                        {{ pro.name }}
                                                                    </a>
                                                                </div>
                                                                <div class="product-rating ">
                                                                    <div class="flex text-[12px] flex-wrap gap-x-[5px]"></div>
                                                                </div>
                                                                <div class="relative pr-9">
                                                                    <div class="price-box">
                                                                        <span class="text-[16px] block font-semibold text-[--price-color]">{{ formatMoney(pro.price_sale) }}</span>
                                                                        <span class="text-[--text-secondary-color] line-through text-[14px] inline-block mr-[5px]">{{ formatMoney(pro.price) }}</span>
                                                                        <div class="inline-block min-w-[44px] w-auto h-auto py-[2px] px-[5px] text-[12px] rounded-full bg-[--label-background] font-medium" style="zoom: 1;">
                                                                            <div class="w-full h-full flex flex-col justify-center items-center text-[--label-color] font-normal">{{ (pro.discount * 100) + '%' }}</div>
                                                                        </div>
                                                                    </div>
                                                                </div>
                                                                <div class="item-color-chosen my-[5px] flex">
                                                                    <div v-for="c2 in colorProduct">
                                                                        <div v-for="c1 in pro.colors">
                                                                            <div class="group/btn-view color-dot relative w-6 h-6 rounded-full m-[5px] cursor-pointer" 
                                                                            style="box-shadow: 0 0 0 1px #eee; transition: box-shadow .25s ease, transform .25s ease;"
                                                                            v-if="c1 === c2.id"
                                                                            :style="`background: url('products/product_color/product-${c2.color}_icon.png') no-repeat center center; background-size: cover;`"
                                                                            >
                                                                                <span class="opacity-0 invisible absolute bottom-full left-1/2 bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] translate-x-[-50%] block w-auto min-w-max
                                                                                                group-hover/btn-view:opacity-100 group-hover/btn-view:visible group-hover/btn-view:bottom-[calc(100%+8px)]
                                                                                                before:content-[''] before:bg-transparent before:absolute before:h-2 before:left-0 before:top-full before:w-full
                                                                                                after:content-[''] after:bg-[#333] after:h-[10px] after:absolute after:w-[10px] after:rotate-45 after:left-[calc(50%-5px)] after:bottom-[-5px]"
                                                                                        style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
                                                                                    >{{ customCapitalize(c2.label) }}</span>
                                                                            </div>
                                                                        </div>    
                                                                    </div>
                                                                    <!-- <a href="#" class="group/btn-more relative w-6 h-6 m-[5px] text-[#888] cursor-pointer">
                                                                        +1
                                                                        <span class="opacity-0 invisible absolute bottom-full left-1/2 bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] translate-x-[-50%] block w-auto min-w-max
                                                                                        group-hover/btn-more:opacity-100 group-hover/btn-more:visible group-hover/btn-more:bottom-[calc(100%+8px)]
                                                                                        before:content-[''] before:bg-transparent before:absolute before:h-2 before:left-0 before:top-full before:w-full
                                                                                        after:content-[''] after:bg-[#333] after:h-[10px] after:absolute after:w-[10px] after:rotate-45 after:left-[calc(50%-5px)] after:bottom-[-5px]"
                                                                                style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
                                                                            >Xem thêm 1 màu khác</span>
                                                                    </a> -->
                                                                </div>
                                                                <span class="max-w-[125px] p-0 mt-2 text-[13px] font-medium overflow-hidden" 
                                                                    style="display: -webkit-box; -webkit-line-clamp: 1; -webkit-box-orient: vertical; white-space: initial;"
                                                                >
                                                                    <img :src="`/products/promo_tag/promo_tag_${pro.promo_tag}.webp`" alt="" class="min-h-[22px] bg-cover bg-center object-contain">
                                                                </span>
                                                            </div>
                                                        </form>
                                                        <div class="pb-[30px]">
                                                            <div
                                                            v-if="(pro.quantity_sale / pro.quantity) < 0.9" 
                                                            class="flashsale__progressbar style2 block w-full h-[6px] bg-[#E9ECEF] mt-[2px] rounded-full relative">
                                                                <div class="text-[12px] relative left-0 z-[2] text-center m-auto h-full text-white flex items-center justify-center gap-x-1">
                                                                    <img src="/products/fire-icon.svg" class="bottom-0 left-[3px] max-w-[24px] max-h-[24px]" alt="">
                                                                    Đã bán
                                                                    <strong>{{ pro.quantity_sale }}</strong>
                                                                    sản phẩm
                                                                </div>
                                                                <div class="h-full bg-[#155BF6] rounded-full absolute top-0 z-[1]" :style="`width: ${ (pro.quantity_sale / pro.quantity) * 100 }%;`"></div>
                                                            </div>
                                                            <div
                                                            v-if="(pro.quantity_sale / pro.quantity) > 0.9" 
                                                            class="flashsale__progressbar style2 block w-full h-[6px] bg-[#E9ECEF] mt-[2px] rounded-full relative">
                                                                <div class="text-[12px] relative left-0 z-[2] text-center m-auto h-full text-white flex items-center justify-center gap-x-1">
                                                                    <img src="/products/fire-icon.svg" class="bottom-0 left-[3px] max-w-[24px] max-h-[24px]" alt="">
                                                                    Sắp cháy hàng
                                                                </div>
                                                                <div class="h-full bg-[#155BF6] rounded-full absolute top-0 z-[1]" :style="`width: ${ (pro.quantity_sale / pro.quantity) * 100 }%;`"></div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </SwiperSlide>
                                        </Swiper>
                                    </div>
                                </Tab>
                                <Tab title="Năng động ngày hè">Hello from Tab 2</Tab>
                                <Tab title="Chào biển nắng mới">Hello from Tab 3</Tab>
                            </TabsWrapper>
                </div>
            </div>
        </div>
    </section>
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

/* Season Coll START */

.ss_item {
    transition: transform 0.64s cubic-bezier(0.15, 0.75, 0.5, 1) 0s;
}

.ss_item:hover {
    transform: scale(1.08) translateZ(0);
}

/* Season Coll END */

/* Flash sale END */

.tab-flashsale {
    width: 100%;
    margin-top: 10px !important;
    overflow-x: auto;
    max-width: 100% !important;
}

.tab-flashsale ul {
    border: 1px solid #eee;
    border-left: none;
    border-right: none;
}

.tab-flashsale .tabs__header li {
    padding: 15px 1rem;
}

.item_product form .product-thumbnail a::before {
    --aspect-ratio: 2/3;
    padding-top: clamp(100%, calc(100vh), calc(100% / (var(--aspect-ratio))));
}

.item_product .item-color-chosen .color-dot:hover {
    box-shadow: 0 0 0 1px #000, inset 0 0 0 4px #fff !important;
    transform: scale(1.1) !important;
}

.item_product .item-color-chosen .color-dot.selected {
    box-shadow: 0 0 0 1px #000, inset 0 0 0 4px #fff !important;
}

.item_product .flashsale__progressbar.style2 {
    height: 20px !important;
    line-height: 20px !important;
}

@media (min-width: 1025px) {
    .item_product form .product-thumbnail:hover {
        box-shadow: 0px 0px 6px 0px rgba(50, 50, 93, 0.1), 1px 1px 5px rgba(0, 0, 0, 0.02);
    }
}

/* Flash sale END */

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

const colorProduct = [
    {  id: 1, color: 'white', label: 'trắng'  },
    {  id: 2, color: 'brown', label: 'nâu'  },
    {  id: 3, color: 'beige', label: 'be'  },
    {  id: 4, color: 'cream', label: 'kem'  },
    {  id: 5, color: 'green', label: 'xanh lá'  },
    {  id: 6, color: 'navy', label: 'navy'  },
    {  id: 7, color: 'black', label: 'đen'  },
];

const products = [ 
    {
        id: 'AT-01', brand: 'Khác', cate: 'T-Shirt', name: 'Áo thun nam - Brown', img_thumbnail: 'product-01.webp', img_hover: 'ao_thun-brown.png', price_sale: 599000, price: 1300000, discount: 0.54, size: [ 'S', 'M', 'L', 'XL' ], colors: [ 2, 5, 1 ], quantity: 300, quantity_sale: 177, promo_tag: 2
    },
    {
        id: 'AT-02', brand: 'Khác', cate: 'T-Shirt', name: 'Áo thun nam - Black', img_thumbnail: 'product-02.webp', img_hover: 'ao_thun-black.png', price_sale: 599000, price: 1300000, discount: 0.54, size: [ 'S', 'M', 'L', 'XL' ], colors: [ 7, 5, 2, 3 ], quantity: 300, quantity_sale: 255, promo_tag: 3
    },
    {
        id: 'AT-03', brand: 'Khác', cate: 'T-Shirt', name: 'Áo thun nam - Cream', img_thumbnail: 'product-03.webp', img_hover: 'ao_thun-cream.png', price_sale: 599000, price: 1300000, discount: 0.54, size: [ 'S', 'M', 'L', 'XL' ], colors: [ 4, 5, 2 ], quantity: 300, quantity_sale: 285, promo_tag: 2
    },
    {
        id: 'AT-04', brand: 'Khác', cate: 'T-Shirt', name: 'Áo thun nam - Green', img_thumbnail: 'product-04.webp', img_hover: 'ao_thun-green.png', price_sale: 399000, price: 1300000, discount: 0.70, size: [ 'S', 'M', 'L', 'XL' ], colors: [ 5, 6, 4 ], quantity: 300, quantity_sale: 192, promo_tag: 2
    },
    {
        id: 'AT-05', brand: 'Khác', cate: 'T-Shirt', name: 'Áo thun nam - White', img_thumbnail: 'product-05.webp', img_hover: 'ao_thun-white.png', price_sale: 599000, price: 1300000, discount: 0.54, size: [ 'S', 'M', 'L', 'XL' ], colors: [ 1, 5, 7 ], quantity: 300, quantity_sale: 192, promo_tag: 2
    },
 ];

 function customCapitalize(value) {
    if (typeof value === 'string') {
        return value.charAt(0).toUpperCase() + value.slice(1);
      }
      return value;
 }

 function formatMoney(value) {
    if (typeof value !== 'number') {
        return value;
    }
    return value.toLocaleString('vi-VN', {
        style: 'currency',
        currency: 'VND'
    });
 }


</script>
