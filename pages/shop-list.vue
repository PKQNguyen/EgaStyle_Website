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
                            <span class="font-normal text-[14px]">Danh sách cửa hàng</span>
                            <span class="font-normal text-[14px]">&nbsp; / &nbsp;</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    <section class="mb-[30px]">
        <div class="m-auto xl:max-w-[1230px] px-[15px] container">
            <h1 class="text-center text-[2rem] py-[10px] font-normal">Danh sách cửa hàng</h1>
            <div class="grid gap-[15px] items-center mt-[30px]" style="grid-template-columns: 350px 1fr;">
                <div id="store" class="flex flex-col relative bg-white py-[30px] px-5 rounded-lg border border-solid border-[#868686] z-[2] drop-shadow-sm">
                    <div class="flex-1 basis-auto min-h-[1px] p-5">
                        <h5 class="font-medium leading-[1.2] text-[25px] mb-[22px] text-[--primary-color)] mt-0">Tìm cửa hàng</h5>
                        <div class="mb-4">
                            <label class="inline-block mb-[15px] font-medium">Chọn tỉnh thành</label>
                            <div>
                                <select name="" id="city" class="form-control">
                                    <option value="Hồ Chí Minh">Hồ Chí Minh</option>
                                    <option value="Hà Nội">Hà Nội</option>
                                </select>
                            </div>
                        </div>
                        <div class="mb-4">
                            <label class="inline-block mb-[15px] font-medium">Chọn cửa hàng</label>
                            <div>
                                <select name="" id="shops" class="form-control">
                                    <option value="Chi nhánh Gò vấp, HCM">Chi nhánh Gò vấp, HCM</option>
                                    <option value="Chi nhánh Phú Nhuận, HCM">Chi nhánh Phú Nhuận, HCM</option>
                                    <option value="Chi nhánh Quận 1, HCM">Chi nhánh Quận 1, HCM</option>
                                    <option value="Chi nhánh Quận 10, HCM">Chi nhánh Quận 10, HCM</option>
                                </select>
                            </div>
                        </div>
                        <div class="my-[30px]">
                            <div class="flex items-start">
                                <div class="mr-[7px] text-[--primary-color]">
                                    <Icon name="ion:location-sharp" class="text-[25px]"></Icon>
                                </div>
                                <div class="flex-1">
                                    <h5 class="text-[25px] mb-[22px] mt-0 text-[--primary-color] font-medium">Địa chỉ</h5>
                                    <div id="shop-infor">
                                        <p class="mt-0 mb-4">150 Nguyễn Duy Cung, phường 15, quận Gò Vấp, HCM</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div id="map"></div>
            </div>
        </div>
    </section>
</template>
<style>

</style>
<script setup>

</script>