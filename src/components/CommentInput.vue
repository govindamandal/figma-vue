<template>
  <div class="relative flex mb-4">
    <span class="absolute inset-y-0 flex items-center">
        <button type="button" class="inline-flex items-center justify-center rounded-full h-12 w-12 transition duration-500 ease-in-out text-gray-500">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5l1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909m-18 3.75h16.5a1.5 1.5 0 001.5-1.5V6a1.5 1.5 0 00-1.5-1.5H3.75A1.5 1.5 0 002.25 6v12a1.5 1.5 0 001.5 1.5zm10.5-11.25h.008v.008h-.008V8.25zm.375 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z" />
          </svg>

        </button>
    </span>
    <input type="text" placeholder="댓글을 남겨주세요." class="w-full focus:outline-none focus:placeholder-gray-400 text-gray-600 placeholder-gray-600 pl-12 bg-gray-200 rounded-md py-3">
    <div class="absolute right-1 items-center inset-y-0 sm:flex">
        <button type="button" class="inline-flex items-center justify-center rounded-lg px-4 py-3 focus:outline-none">
          <span class="font-bold">등록</span>
        </button>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'CommentInput'
  }
</script>