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
                        <li>
                            <a href="/index" class="text-[--link-color]"><span class="font-normal text-[14px]">Tài khoản</span></a>
                            <span class="font-normal text-[14px]"> &nbsp; / &nbsp;</span>
                        </li>
                        <li class="active">
                            <span class="font-normal text-[14px]">Quên mật khẩu</span>
                            <span class="font-normal text-[14px]">&nbsp; / &nbsp;</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
    <section class="section">
        <div class="container relative flex flex-col py-5 mb-5">
            <div class="page_login">
                <div class="text-center heading-bar">
                    <h1 class="mb-0 py-[10px] font-normal text-[25px] leading-tight uppercase">ĐĂNG NHẬP TÀI KHOẢN</h1>
                    <p class="mb-0">
                        Bạn chưa có tài khoản ?
                        <NuxtLink to="/account/sign-up" class="underline text-[#2F80ED]"> Đăng ký tại đây</NuxtLink>
                    </p>
                </div>
                <div class="mx-[-15px] flex flex-wrap">
                    <div class="py-4 mx-auto lg:basis-1/3 md:basis-3/12">
                        <div class="page-forgot_password">
                            <div class="forgot_password">
                                <h2 class="text-center uppercase text-[18px] mb-5">ĐẶT LẠI MẬT KHẨU</h2>
                                <p class="text-center">Chúng tôi sẽ gửi cho bạn một email để kích hoạt việc đặt lại mật khẩu.</p>
                                <form action="/">
                                    <div class="form-forgot_password">
                                        <fieldset class="mb-4 form-group">
                                            <label class="mb-2 inline-block mt-0 font-semibold text-[14px]">Email: <span class="text-[#f00]">*</span></label>
                                            <input type="email" class="form-control" name="email" id="customer_email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,63}$" placeholder="Email" required>
                                        </fieldset>
                                        <div class="flex flex-col items-center justify-center mb-4">
                                            <button class="relative w-full mb-2 rounded-md btn btn-login" value="Đăng nhập">Lấy lại mật khẩu</button>
                                            <NuxtLink to="/">Quay lại</NuxtLink>
                                        </div>
                                    </div>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="float-left w-full mt-5 text-center">
                <p class="text-[#6c757d]">Hoặc đăng nhập bằng</p>
            </div>
        </div>
    </section>
</template>
<style>

</style>
<script setup>

</script>