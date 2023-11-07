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
                            <span class="font-normal text-[14px]">Đăng nhập</span>
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
                    <h1 class="mb-0 py-[10px] font-normal text-[25px] leading-tight uppercase">Đăng nhập tài khoản</h1>
                    <p class="mb-0">
                        Bạn chưa có tài khoản ?
                        <NuxtLink to="/account/sign-up" class="underline text-[#2F80ED]"> Đăng ký tại đây</NuxtLink>
                    </p>
                </div>
                <div class="mx-[-15px] flex flex-wrap">
                    <div class="py-4 mx-auto lg:basis-1/3 md:basis-3/12">
                        <div class="page-login">
                            <div class="login">
                                <form action="/">
                                    <div class="form-signup">
                                        <fieldset class="mb-0 form-group">
                                            <label class="mb-2 inline-block mt-0 font-semibold text-[14px]">Email: <span class="text-[#f00]">*</span></label>
                                            <input type="email" class="form-control" name="email" id="customer_email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,63}$" placeholder="Email" required>
                                        </fieldset>
                                        <fieldset class="mb-0 form-group">
                                            <label class="mb-2 inline-block mt-0 font-semibold text-[14px]">Mật khẩu: <span class="text-[#f00]">*</span></label>
                                            <input type="password" class="form-control" name="password" id="customer_password" placeholder="Mật khẩu" required>
                                            <small class="block my-2">
                                                Quên mật khẩu? Nhấn vào
                                                <NuxtLink to="/account/forgot-password" class="text-[#2F80ED]">đây</NuxtLink>
                                            </small>
                                        </fieldset>
                                        <div class="mb-4">
                                            <button class="relative w-full rounded-md btn btn-login" value="Đăng nhập">Đăng nhập</button>
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