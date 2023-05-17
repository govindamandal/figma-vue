<template>
  <div class="flex flex-col mb-2 ml-4 mt-1">
    <div v-for="(comment, c) in comments" :key="c">
      <div class="flex flex-row mt-2 px-2">
        <div class="w-auto h-auto rounded-full border-2 border-pink-500">
          <img class='w-12 h-12 object-cover rounded-full shadow cursor-pointer' alt='User avatar' :src='comment.avatar'>
        </div>
        <div class="flex flex-col mb-2 ml-3 mt-1">
          <div class='text-gray-600 text-sm font-semibold'>
            <span>{{ comment.user }}</span>
          </div>
        </div>
        <div class="flex flex-row mb-2 ml-4 mt-1">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="w-4 h-4 bg-green-700 rounded-lg text-white font-bold">
            <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5" />
          </svg>
          <span class='text-slate-500 font-thin text-xs ml-2'>
            1일전
          </span>
        </div>
      </div>
      <div class='text-gray-500 font-thin text-sm mb-6 ml-16 mx-3 px-2'>
        <p class="mt-2">{{ comment.comment }}</p>
        <div class="flex justify-start mx-5 reaction-section">
          <p class="flex flex-row mr-4">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 mr-1">
              <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z" />
            </svg>
            <span class="text-xs reaction-count">5</span>
          </p>
          <p class="flex flex-row">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 mr-1">
            <path stroke-linecap="round" stroke-linejoin="round" d="M8.625 12a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0H8.25m4.125 0a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0H12m4.125 0a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0h-.375M21 12c0 4.556-4.03 8.25-9 8.25a9.764 9.764 0 01-2.555-.337A5.972 5.972 0 015.41 20.97a5.969 5.969 0 01-.474-.065 4.48 4.48 0 00.978-2.025c.09-.457-.133-.901-.467-1.226C3.93 16.178 3 14.189 3 12c0-4.556 4.03-8.25 9-8.25s9 3.694 9 8.25z" />
          </svg>
          <span class="text-xs reaction-count">5</span>
          </p>
        </div>
        <Comments v-if="comment.replies.length" :comments="comment.replies" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Comments',
  props: {
    comments: {
      type: Array,
      default: []
    }
  }
}
</script>