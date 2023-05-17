<template>
  <div class='text-gray-400 font-medium text-sm mb-7 mt-6 mx-3 px-2'><img class="rounded" src="https://picsum.photos/536/354"></div>
</template>
<script>
  export default {
    name: 'Banner',
    props: {
      banner: {
        type: String,
        required: true
      }
    }
  }
</script>