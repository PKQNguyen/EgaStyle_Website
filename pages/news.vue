<template>
    <section class="mb-4 mt-2 bg-[#f6f6f6] text-[#999] block">
        <span class="text-[14px] font-normal"></span>
        <div class="px-[15px] xl:max-w-[1230px] m-auto">
            <div class="mx-[-15px] flex flex-wrap">
                <div class="px-[15px] flex basis-full max-w-full">
                    <ul class="flex flex-wrap m-0 px-0 py-1 bg-[#f6f6f6]">
                        <li>
                            <a href="/index" class="text-[--link-color]"><span class="font-normal text-[14px]">Trang chủ</span></a>
                            <span class="font-normal text-[14px]"> &nbsp; / &nbsp;</span>
                        </li>
                        <li class="active">
                            <span class="font-normal text-[14px]">Tin tức</span>
                            <span class="font-normal text-[14px]">&nbsp; / &nbsp;</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    <section class="mb-[30px]">
        <div class="m-auto xl:max-w-[1230px] px-[15px] container">
            <h1 class="text-center text-[2rem] py-[10px] font-normal my-[30px] mx-auto">Tin tức</h1>
            <div class="flex flex-wrap mx-[-15px] pt-[30px] border border-solid border-[#eee]">
                <div class="lg:basis-3/4 lg:max-w-[75%] flex px-[15px]">
                    <div class="mx-[-15px] flex flex-wrap">
                        <div class="px-[15px] basis-full max-w-full flex" v-for="n in news">
                            <div class="grid gap-[30px]" style="grid-template-columns: 2fr 3fr;">
                                <a href="#" class="flex items-center justify-center relative text-center overflow-hidden rounded-md aspect-[433/231]" :title="`${n.title}`">
                                    <img :src="`/news/${n.thumbnail}`" class="w-auto m-auto max-h-auto" :alt="`${n.title}`">
                                </a>
                                <div class="mb-[7px] text-[#6c757d] py-2 ">
                                    <h3 class="font-normal leading-[1.2] text-[1.25rem]">
                                        <a href="#" class="font-normal leading-[1.2] text-[1.25rem] link" >{{ n.title }}</a>
                                    </h3>
                                    <div class="leading-[1.4] flex items-start">
                                        <div class="flex gap-[10px] items-center flex-wrap mb-[5px] flex-1">
                                            <div class="text-[14px] flex items-center gap-[10px] my-[10px] text-[#6c757d]">
                                                <span class="inline-flex items-center gap-[5px]">
                                                    <Icon name="ion:calendar" class="text-[22px]"></Icon>
                                                    {{ n.createDate }}
                                                </span>
                                                <span class="inline-flex items-center gap-[5px]">
                                                    <Icon name="ion:md-clock" class="text-[22px]"></Icon>
                                                    {{ n.minutesRead }} phút đọc
                                                </span>
                                            </div>
                                        </div>
                                    </div>
                                    <p class="mt-0 mb-4">
                                        <span>{{ n.desc }}</span>
                                        <a href="#" class="block mt-[10px] text-[14px] underline link" title="Đọc tiếp">
                                            Đọc tiếp
                                        </a>
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="lg:basis-1/4 lg:max-w-[25%] flex px-[15px] pb-5">
                    <aside class="block pt-[15px] w-full">
                        <div>
                            <h2 class="font-bold text-[1rem] mb-[14px] uppercase leading-[1.2]">
                                <span>Danh mục tin tức</span>
                            </h2>
                        </div>
                        <div class="relative text-[14px] p-0 border-b-0">
                            <nav class="block">
                                <ul class="flex flex-col flex-wrap pb-0 pl-0">
                                    <li class="relative"><a href="/" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Trang chủ</a></li>
                                    <li class="relative flex items-center justify-between">
                                        <a href="/" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Sản phẩm</a>
                                        <Icon name="ion:md-arrow-dropdown" class="text-[27px]"></Icon>
                                    </li>
                                    <li class="relative flex items-center justify-between">
                                        <a href="/" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Chương trình khuyến mãi</a>
                                        <Icon name="ion:md-arrow-dropdown" class="text-[27px]"></Icon>
                                    </li>
                                    <li class="relative mt-2"><a href="/shoplist" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Hệ thống cửa hàng</a></li>
                                    <li class="relative mt-2"><a href="/aboutus" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Giới thiệu</a></li>
                                    <li class="relative mt-2"><a href="/news" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Tin tức</a></li>
                                    <li class="relative mt-2"><a href="/" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Liên hệ</a></li>
                                    <li class="relative mt-2"><a href="/" class="text-[1rem] font-normal leading-[1.3] pt-[5px] pr-[30px] pb-[2px] link" style="color: #666;">Kiểm tra đơn hàng</a></li>
                                </ul>
                            </nav>
                        </div>
                    </aside>
                </div>
            </div>
        </div>
    </section>
</template>
<style>

</style>
<script setup>
const news = [
    { id: 0, title: 'Quần short nam và 5 nguyên tắc nam giới cần phải biết', thumbnail: 'news_1.jpg', createDate: 'Th 4 12/04/2023', minutesRead: 3, desc: 'Những mẫu quần short luôn là một trong những items thời trang chiếm số lượng cực lớn trong tủ đồ của mọi chàng trai. Hãy cùng...' },
    { id: 1, title: '9 Cách phối màu quần áo nam cho chàng thêm phong cách và thời trang', thumbnail: 'news_2.jpg', createDate: 'Th 3 11/04/2023', minutesRead: 6, desc: 'Chọn trang phục có thiết kế đẹp và hợp với dáng thôi vẫn chưa đủ đâu nhé các chàng trai. Để có một set đồ ấn...' },
    { id: 2, title: 'Bí mật 6+ cách phối đồ ăn gian chiều cao cho nam đơn giản, hiệu quả cao', thumbnail: 'news_3.webp', createDate: 'Th 3 11/04/2023', minutesRead: 8, desc: 'Cách phối đồ ăn gian chiều cao cho nam giới là vấn đề được phái mạnh quan tâm nhiều nhất. Xã hội luôn thích những người...' },
    { id: 3, title: '8 Xu hướng thời trang nam mùa hè mới nhất', thumbnail: 'news_4.webp', createDate: 'Th 3 11/04/2023', minutesRead: 7, desc: 'Mùa hè năm nổ ra nhiều xu hướng thời trang nam mới hướng tới sự thoái mái và năng động. Từ những gam màu nóng nổi...' },
    { id: 4, title: 'TOP 4 ITEM QUẦN ÁO NAM MÙA HÈ GÂY BÃO CỰC CHẤT', thumbnail: 'news_5.webp', createDate: 'Th 3 11/04/2023', minutesRead: 4, desc: 'Thời trang là khẳng định phong cách, là yếu tố tôn lên vẻ đẹp tiềm ẩn của mỗi cá nhân. Chính vì vậy, làng thời trang...' },
];
</script>