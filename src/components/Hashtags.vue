<template>
  <div class="px-2 mx-2 ml-3">
    <button v-for="(hash, h) in hashtags" :key="h" type="button" class="rounded-md mr-2 px-4 btn-hashtag">{{ hash }}</button>
  </div>
</template>
<script>
  export default {
    name: 'Hashtags',
    data: () => {
      return {
        hashtags: ['#2023', '#TODAYISMONDAY', '#TOP', '#POPS!', '#WOW', '#ROW']
      }
    }
  }
</script>