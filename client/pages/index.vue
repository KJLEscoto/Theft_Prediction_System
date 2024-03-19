<template lang="">
  <div class="bg-[url('assets/img/bg/login-bg.jpg')] bg-center bg-cover bg-no-repeat h-screen w-full bg-black">
    <div class="flex items-center lg:justify-start justify-center h-screen lg:p-24 p-0">
      <form class="h-auto lg:w-1/2 w-3/4 bg-[#0C0F12] rounded shadow shadow-[#1C2E39] p-5 text-[#557479] tracking-wider">
          <h1 class="cursor-default font-bold text-2xl mb-5 text-center">User Authentication</h1>
          <div class="px-5 mb-5">   
            <hr class="mb-5 border-[#557479]">
            <label class="text-base">Username</label>
            <input type="text" class="w-full bg-[#96a9ac] focus:bg-[#dbe2e3] py-2 px-3 rounded border border-black transition-all duration-300 outline-none focus:border-[#557479] text-black mb-5 mt-1">
            <label class="text-base">Password</label>
            <input type="password" class="w-full bg-[#96a9ac] focus:bg-[#dbe2e3] py-2 px-3 rounded border border-black transition-all duration-300 outline-none focus:border-[#557479] text-black mb-2 mt-1">
            <p class="text-xs mb-3 text-end"><nuxt-link to="/">Forgot password?</nuxt-link></p>
            <nuxt-link to="verified/main-page">
              <button type="submit" class="w-full text-center bg-[#67171D] py-2 rounded mt-2 text-white tracking-wider opacity-90 hover:opacity-100 font-semibold">Login</button>
            </nuxt-link>
          </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {

}
</script>