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
                            <span class="font-normal text-[14px]">Liên hệ</span>
                            <span class="font-normal text-[14px]">&nbsp; / &nbsp;</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    <section class="mb-[30px]">
        <div class="m-auto xl:max-w-[1230px] px-[15px] container py-4">
            <div class="mx-[-15px] flex flex-wrap">
                <div class="lg:basis-1/2 lg:max-w-[50%] px-[15px] flex">
                    <div class="w-full lg:px-2">
                        <h1 class="mb-4 text-[2rem] py-[10px] font-normal">Công ty TNHH EGANY</h1>
                        <div class="flex items-center text-[14px] mb-[5px] gap-2">
                            <Icon name="ion:location-sharp" class="text-[24px]"></Icon>
                            <div>Địa chỉ: <span>150/8 Nguyễn Duy Cung, Phường 12, Tp.HCM</span></div>
                        </div>
                        <div class="flex items-center text-[14px] mb-[5px] gap-2">
                            <Icon name="ion:ios-telephone" class="text-[24px]"></Icon>
                            <div>Số điện thoại: <a href="#" class="link">19001393</a></div>
                        </div>
                        <div class="flex items-center text-[14px] mb-[5px] gap-2">
                            <Icon name="ion:ios-mail" class="text-[24px]"></Icon>
                            <div>Email: <a href="#" class="link">support@egany.com</a></div>
                        </div>
                        <div class="pt-4 mt-4 border-t">
                            <h2 class="text-[1rem] mb-[14px] uppercase font-normal">Liên hệ với chúng tôi</h2>
                            <form action="/">
                                <div>
                                    <div class="flex flex-wrap mx-[-15px]">
                                        <fieldset class="px-[15px] mb-4 lg:basis-full lg:max-w-full">
                                            <input class="form-control text-[1rem]" type="text" placeholder="Họ tên*">
                                        </fieldset>
                                        <fieldset class="px-[15px] mb-4 lg:basis-full lg:max-w-full">
                                            <input class="form-control text-[1rem]" type="email" placeholder="Email*">
                                        </fieldset>
                                        <fieldset class="px-[15px] mb-4 lg:basis-full lg:max-w-full">
                                            <input class="form-control text-[1rem]" type="text" placeholder="Số điện thoại*">
                                        </fieldset>
                                        <fieldset class="px-[15px] mb-4 lg:basis-full lg:max-w-full">
                                            <textarea class="form-control text-[1rem]" placeholder="Nhập nội dung*" name="" id="comments" rows="5" style="height: 130px;" required></textarea>
                                        </fieldset>
                                        <div class="px-[15px] basis-full max-w-full">
                                            <button class="block w-full text-white bg-black rounded-md btn" type="submit">Gửi liên hệ của bạn</button>
                                        </div>
                                    </div>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
                <div class="lg:basis-1/2 lg:max-w-[50%] px-[15px] flex">
                    <div id="map" class="relative w-full h-full overflow-hidden">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3928.842949738566!2d105.75038727459496!3d10.029815672521869!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31a08830e54e5f25%3A0xd7d159025caa8609!2zxJAuIE5ndXnhu4VuIFbEg24gTGluaCwgTmluaCBLaeG7gXUsIEPhuqduIFRoxqEsIFZpZXRuYW0!5e0!3m2!1sen!2s!4v1697089835819!5m2!1sen!2s" width="600" style="border:0; width: 100%; height: 100%; border-radius: 10px;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style>

</style>
<script setup>

</script>