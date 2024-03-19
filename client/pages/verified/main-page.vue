<template lang="">
  <div class="h-screen w-full bg-[#0E1213] p-3 tracking-wide">

    <nav class="h-14 w-full bg-[#1C242B] rounded flex items-center p-3 justify-between shadow-lg">
      <!-- <p class="text-black font-semibold">Main Page</p> -->
      <div class="flex gap-4 text-[#a7b7ba]">
        <p class="">Check Log</p>
        <p class="">History</p>
        <p class="">Help</p>
      </div>
      <div class="flex justify-between items-center">
        <div class="bg-[#E5EEC1] p-1 rounded shadow-lg cursor-pointer">
          <img class="w-auto h-6" src="/assets/img/icons/notification.png" alt="notification"/>
        </div>
      </div>
    </nav>

    <div class="mt-2 h-5/6 h- w-full grid grid-cols-7 gap-2">
      <div class="bg-[#898989] rounded p-1 col-span-6 justify-center flex items-center">
        <p class="text-red-800">Camera not found</p>
      </div>

      <div class="bg-[#1C242B] p-3 w-full h-auto rounded">
        <div class="bg-[#185552] p-4 rounded">
          <p class="text-white mb-2">System</p>
          <hr>
          <div class="flex gap-3 mt-3 justify-center">
            <div class="bg-[#E5EEC1] px-3 py-1 rounded shadow-lg cursor-pointer">
              <img class="w-auto h-6 m-auto" src="/assets/img/icons/settings.png"/>
              <p class="text-xs font-semibold">Settings</p>
            </div>
            <div class="bg-[#E5EEC1] px-4 py-1 rounded shadow-lg cursor-pointer">
              <img class="w-auto h-6 m-auto" src="/assets/img/icons/profile.png"/>
              <p class="text-xs font-semibold">Profile</p>
            </div>
          </div>
        </div>
        <div class="bg-[#185552] p-4 rounded mt-3">
          <p class="text-white mb-2">Camera Control</p>
          <hr>
          <p class="text-white text-sm tracking-widest mt-2">Brightness</p>
          <div class="w-full flex justify-between gap-2 mt-2">
            
            <div class="bg-[#557C83] rounded shadow-lg p-1">
              <img class="w-5 h-full" src="/assets/img/icons/b-down.png" alt="down"/>
            </div>
            <input type="range" class="w-full h-1 bg-gray-300 rounded-md appearance-none outline-none opacity-70 transition-opacity duration-200 hover:opacity-100 m-auto" min="0" max="100" step="1">
            <div class="bg-[#557C83] rounded shadow-lg p-1">
              <img class="w-5 h-full" src="/assets/img/icons/b-up.png" alt="up"/>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>


<script setup>

</script>