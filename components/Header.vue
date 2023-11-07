<template>
    <div class="relative bg-[#81AACC]">
        <div class="px-0 text-center">
            <a href="#" class="relative block text-[#ffffff] uppercase h-10 leading-10" title="FREESHIP VỚI ĐƠN HÀNG TỪ 500K">
                Free Ship Với Đơn Hàng Từ 500k	
            </a>
            <button 
            class="
                absolute right-2 top-[5px] bg-white w-[25px] h-[25px] rounded-full 
                flex items-center justify-center cursor-pointer
                close">
                <Icon name="ion:close-sharp" />
            </button>
        </div>
    </div>
    <header class="sticky top-0 z-10 block bg-white shadow-md">
        <div class="px-[15px] lg:max-w-[1230px] h-[65px] grid items-center gap-[15px] m-auto" style="grid-template-columns: 150px 1fr 150px;">
            <div class="logo">
                <a href="">
                    <img class="h-auto max-w-full" src="/logo.webp" alt="logo EGA Men Style" width="134" height="45" srcset="">
                </a>
            </div>
            <div class="items-center justify-center hidden w-full lg:flex">
                <div class="overflow-hidden max-h-[65px]">
                    <nav>
                        <ul class=" h-[313px] min-h-full max-w-full w-full overflow-x-hidden flex flex-row flex-wrap rounded-none">
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <a href="/" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Trang chủ">
                                    <span>Trang chủ</span>
                                </a>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <NuxtLink to="/" 
                                class="no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative
                                    peer/btn-mega-menu hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Sản phẩm">
                                    <span>Sản phẩm</span>
                                    <Icon name="ion:chevron-down" class="ml-[6px]" />
                                </NuxtLink>
                                <div class=" hidden w-full h-[320px] py-[14px] px-5 rounded-none absolute bottom-0 top-full left-0 bg-white ml-0 shadow-md z-10 overflow-auto text-[1rem]
                                            lg:peer-hover/btn-mega-menu:block g:peer-hover/btn-mega-menu:z-[900] lg:hover:block lg:hover:z-[900]">
                                    <ul class="lg:max-w-[1230px] m-auto grid grid-cols-4 gap-y-[10px] gap-x-[5px] p-0">
                                        <li class="flex flex-col items-start text-[1rem]">
                                            <span class="mb-1 font-semibold">
                                                <a href="#" class="link" title="Bộ sưu tập">Bộ sưu tập</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo khoác">Áo khoác</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo sơ mi">Áo sơ mi</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo thun">Áo thun</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Quần dài">Quần dài</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Quần jeans">Quần jeans</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Quần short">Quần short</a>
                                            </span>
                                        </li>
                                        <li class="flex flex-col items-start text-[1rem]">
                                            <span class="mb-1 font-semibold">
                                                <a href="#" class="link" title="Mặc theo dịp">Mặc theo dịp</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Dạo phố">Dạo phố</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đi biển">Đi biển</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Du lịch">Du lịch</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đi chơi">Đi chơi</a>
                                            </span>
                                        </li>
                                        <li class="flex flex-col items-start text-[1rem]">
                                            <span class="mb-1 font-semibold">
                                                <a href="#" class="text-[#666666] link" title="Áo nam thời trang">Áo nam thời trang</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo thể thao">Áo thể thao</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo sơ mi">Áo sơ mi</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo khoác">Áo khoác</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Áo thun">Áo thun</a>
                                            </span>
                                        </li>
                                        <li class="flex flex-col items-start text-[1rem]">
                                            <span class="mb-1 font-semibold">
                                                <a href="#" class="text-[#666666] link" title="Đồ mặc nhà">Đồ mặc nhà</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đồ dài">Đồ dài</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đồ ngắn">Đồ ngắn</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đồ xuân - hè">Đồ xuân - hè</a>
                                            </span>
                                            <span class="mb-1">
                                                <a href="#" class="text-[#666666] link" title="Đồ thu - đông">Đồ thu - đông</a>
                                            </span>
                                        </li>
                                    </ul>
                                </div>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <a href="#" 
                                class="no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color] peer/btn-page
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Sản phẩm">
                                    <img src="/menu_icon_3.png" class="object-contain mr-1 max-w-6 max-h-6" alt="Chương trình khuyến mãi">
                                    <span>Chương trình khuyến mãi</span>
                                    <Icon name="ion:chevron-down" class="ml-[6px]" />
                                </a>
                                <div class="hidden w-[250px] h-auto py-[14px] px-5 rounded-none absolute bottom-0 top-full left-0 bg-white ml-0 shadow-md z-10 overflow-auto text-[1rem] 
                                            lg:peer-hover/btn-page:block lg:peer-hover/btn-page:z-[900] hover:block hover:z-[900]" 
                                    style="bottom: initial; left: inherit;">
                                    <ul class="lg:max-w-[1230px] m-auto flex flex-col gap-x-[10px] gap-y-[5px] p-0">
                                        <li><a href="#" class="link" title="Landing Page - XMas">Landing Page - XMas</a></li>
                                        <li><a href="#" class="link" title="Landing Page - Black Friday">Landing Page - Black Friday</a></li>
                                        <li><a href="#" class="link" title="Landing Page - OnePage">Landing Page - OnePage</a></li>
                                        <li><a href="#" class="link" title="Landing Page - Flash Sale">Landing Page - Flash Sale</a></li>
                                    </ul>
                                </div>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <NuxtLink to="/shop-list" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Hệ thống cửa hàng">
                                    <span>Hệ thống cửa hàng</span>
                                </NuxtLink>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <NuxtLink to="/about-us" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Giới thiệu">
                                    <span>Giới thiệu</span>
                                </NuxtLink>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <NuxtLink to="/news" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Tin tức">
                                    <span>Tin tức</span>
                                </NuxtLink>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <NuxtLink to="/contact-us" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Liên hệ">
                                    <span>Liên hệ</span>
                                </NuxtLink>
                            </li>
                            <li class="p-0 bg-transparent border-b-0 border-x-0 menu-item" :class="{'translate-y-[-100%]': menuStatus}">
                                <a href="#" 
                                class=" no-underline whitespace-nowrap flex items-center py-5 px-[15px] relative hover:text-[--primary-color]
                                    after:contents-['*']  after:h-[2px] after:w-0 after:overflow-hidden after:absolute left-4 after:bottom-[15px] after:bg-black after:transition-[width] ease-in-out duration-1000
                                    menu-item__link" title="Kiểm tra đơn hàng">
                                    <span>Kiểm tra đơn hàng</span>
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <div class="flex items-center">
                    <button class="flex items-center justify-center w-10 h-10 cursor-pointer hover:bg-gray-100 hover:rounded-full" :class="{'disabled': !menuStatus}" @click="changeMenu()"><Icon name="ion:chevron-left" class="font-black text-[22px]"/></button>
                    <button class="flex items-center justify-center w-10 h-10 cursor-pointer hover:bg-gray-100 hover:rounded-full" :class="{'disabled': menuStatus}" @click="changeMenu()"><Icon name="ion:chevron-right" class="font-black text-[22px]"/></button>
                </div>
            </div>
            <div class="flex justify-end">
                <div class="grid w-full grid-cols-4 text-2xl text-center" >
                    <span class="flex items-center justify-center"><Icon name="ion:search" class="text-[30px]"></Icon></span>
                    <div class="relative hidden lg:block md:block group/btn-login">
                        <Icon name="ion:person-outline" class="inline-block font-black text-[30px]"></Icon>
                        <div class="opacity-0 absolute invisible top-[calc(100%+10px)] left-1/2 bg-[#333] py-[5px] px-2 rounded-[5px] text-white text-[12px] translate-x-[-50%] block w-[95px] h-[70px] text-left
                                    group-hover/btn-login:opacity-100 group-hover/btn-login:visible group-hover/btn-login:bottom-[calc(100%+8px)]
                                    before:content-[''] before:bg-transparent before:absolute before:h-[10px] before:left-0 before:bottom-full before:w-full
                                    after:content-[''] after:bg-[#333] after:h-[14px] after:absolute after:w-[14px] after:rotate-45 after:left-[calc(50%-7px)] after:top-[-7px] after:z-[-1]"
                            style="transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);"
                        >
                            <NuxtLink to="/account/sign-in" class="inline-block px-2 outline-none" title="Đăng nhập">Đăng nhập</NuxtLink>
                            <NuxtLink to="/account/sign-up" class="inline-block px-2 outline-none" title="Đăng ký">Đăng ký</NuxtLink>
                        </div>
                    </div>
                    <a href="#" class="relative text-[22px]">
                        <Icon name="ion:heart-outline" class="align-top text-[30px]"></Icon>
                        <span class="absolute inline-block bg-[#da3f3f] rounded-full w-5 h-5 leading-[20px] text-white text-[12px] top-[2px] right-0">2</span>
                    </a>
                    <div class="relative sm:text-center group/btn-cart">
                        <a href="#" class="relative text-[22px]" title="Giỏ hàng">
                            <Icon name="ion:bag-handle-outline" class="align-top text-[30px]"></Icon>
                            <span class="absolute inline-block bg-[#da3f3f] rounded-full w-5 h-5 leading-[20px] text-white text-[12px] top-[-2px] right-[-5px]">2</span>
                        </a>
                        <div class="absolute z-[-1] invisible opacity-0 w-[400px] right-0 top-[calc(100%+8px)] text-black py-[10px] px-[15px] text-[14px] rounded-[0.25rem] border border-solid border-[#00000014] flex bg-white flex-col
                                    before:content-[''] before:w-0 before:h-0 before:border-solid before:border-x-[7.5px] before:border-b-[10px] before:border-x-transparent before:border-t-transparent before:border-b-[#fff] before:absolute before:top-[-9px] before:right-[15px]
                                    after:content-[''] after:w-full after:h-full after:absolute after:top-[9px] after:z-0
                                    lg:group-hover/btn-cart:z-[199] lg:group-hover/btn-cart:visible lg:group-hover/btn-cart:opacity-100 lg:group-hover/btn-cart:drop-shadow-md"
                        >
                            <ul class="list-none p-0 mb-0 z-[1] relative">
                                <div class="text-center">
                                    <p class="m-auto">Không có sản phẩm nào.</p>
                                </div>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style>
    .menu-item:hover > .menu-item__link::after {
        width: calc(100% - 30px);
    }

    button.disabled {
        cursor: not-allowed;
    }
</style>
<script setup>
import { ref } from 'vue';
var menuStatus = ref(true); 

function changeMenu() {
    menuStatus.value = !menuStatus.value;
}

const menu = [
    
];
</script>