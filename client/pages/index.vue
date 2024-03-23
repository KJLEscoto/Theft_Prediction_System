<template>
  <div class="bg-[url('assets/img/bg/login-bg.jpg')] bg-center bg-cover bg-no-repeat h-screen w-full bg-black">
    <div class="flex items-center lg:justify-start justify-center h-screen lg:p-24 p-0 duration-300">
      <transition name="slide" appear>
        <form
          class="h-auto lg:w-1/2 w-3/4 bg-[#00030c] rounded shadow-2xl shadow-[#1c2e3998] p-5 text-[#b8c5c7] tracking-wider">
          <div class="flex items-center gap-1 mb-5 justify-center">
            <Icon icon="material-symbols:shield-person" class="w-auto h-10" />
            <h1 class="cursor-default font-bold text-2xl">User Authentication</h1>
          </div>
          <div class="px-5 mb-5">
            <hr class="mb-5 border-[#557479]">
            <div>
              <div class="flex gap-1 items-center">
                <Icon icon="material-symbols:person" class="w-auto h-5" />
                <label for="username" class="text-base">Username</label>
              </div>
              <input name="username" type="text"
                class="w-full bg-[#96a9ac] focus:bg-[#dbe2e3] py-2 px-3 rounded border border-black transition-all duration-300 outline-none focus:border-[#557479] text-black mb-5 mt-1">
            </div>
            <div>
              <div class="flex items-center gap-1">
                <Icon icon="solar:lock-password-unlocked-bold" class="w-auto h-5" />
                <label class="text-base">Password</label>
              </div>
              <span class="flex items-center relative">
                <input :type="passwordFieldType" ref="passwordInput" @focus="isInputFocused = true"
                  @blur="isInputFocused = false"
                  class="w-full bg-[#96a9ac] focus:bg-[#dbe2e3] py-2 px-3 pr-12 rounded border border-black transition-all duration-300 outline-none focus:border-[#557479] text-black mb-2 mt-1">
                <span
                  class="absolute right-0 cursor-pointer mr-3 text-black hover:bg-[#758e92] hover:text-[#b8c5c7] p-1 rounded-full duration-150">
                  <Icon @click="showPassword" icon="ic:outline-remove-red-eye" class="w-auto h-5" />
                </span>
              </span>
            </div>
            <div class="flex gap-1 items-center w-auto">
              <nuxt-link to="/auth/main-page">
                <span class="hover:opacity-50 flex gap-1 items-center">
                  <Icon icon="tabler:lock-question" class="w-auto h-3" />
                  <span class="text-xs">Forgot password?</span>
                </span>
              </nuxt-link>
            </div>

            <nuxt-link to="auth/main-page">
              <button type="submit"
                class="mt-5 w-full text-center bg-[#67171D] py-2 rounded text-white tracking-wider opacity-90 hover:opacity-100 font-semibold">Login</button>
            </nuxt-link>
          </div>
        </form>
      </transition>
    </div>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';

const passwordFieldType = ref('password');
const isInputFocused = ref(false);
const passwordInput = ref(null);

const showPassword = () => {
  passwordFieldType.value = passwordFieldType.value === 'password' ? 'text' : 'password';
  if (passwordFieldType.value === 'text' || 'password') {
    passwordInput.value.focus();
  }
};

</script>
