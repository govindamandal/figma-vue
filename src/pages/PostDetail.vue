<template>
  <div class='flex max-w-xl bg-white mx-auto'>
    <div class='flex items-center w-full'>
      <div class='w-full'>
        <div class="flex flex-row mt-2 px-2 py-3 mx-3">
          <div class="w-auto h-auto rounded-full border-2 border-pink-500">
            <img class='w-12 h-12 object-cover rounded-full shadow cursor-pointer' alt='User avatar' src='https://en.gravatar.com/userimage/100383909/61e19fd27a19e420a4251098c3939def.png'>
          </div>
          <!-- Editor -->
          <div class="flex flex-col mb-2 ml-4 mt-1">
            <div class='text-gray-600 text-sm font-semibold'>
              <span>안녕 나 응애</span>
            </div>
            <div class='flex w-full mt-1'>
              <div class='text-slate-500 font-base text-xs mr-1 cursor-pointer'>
                165cm . 53kg
              </div>
            </div>
          </div>
          <!-- Time of the post -->
          <div class="flex flex-row mb-2 ml-4 mt-1">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="w-4 h-4 bg-green-700 rounded-lg text-white font-bold">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5" />
            </svg>
            <span class='text-slate-500 font-thin text-xs ml-2'>
              1일전
            </span>
          </div>
        </div>
        
        <div class='text-gray-600 font-semibold text-lg mb-2 mx-3 px-2'>
          지난 월요일에 했던 이벤트 중 가장 괜찮은 상품 뭐야?
        </div>
        <div class='text-gray-500 font-thin text-sm mb-6 mx-3 px-2'>
          <p class="mt-2">지난 월요일에 2023년 S/S 트렌드 알아보기 이벤트 참석했던 팝들아~ 혹시 어떤 상품이 제일 괜찮았어?</p>
          <p class="mt-2">후기 올라오는거 보면 로우라이즈? 그게 제일 반응 좋고 그 테이블이 제일 재밌었다던데 맞아???</p>
          <p class="mt-2">올해 로우라이즈가 트렌드라길래 나도 도전해보고 싶은데 말라깽이가 아닌 사람들도 잘 어울릴지 너무너무 궁금해ㅜㅜ로우라이즈 테이블에 있었던 팝들 있으면 어땠는지 후기 좀 공유해주라~~!</p>
        </div>
        <!-- Hashtags -->
        <Hashtags />
        <Banner />
        <Reaction />
        <Comments :comments="comments"/>
      </div>
    </div>
  </div>
</template>
<script>
  import Banner from '../components/Banner.vue'
  import Comments from '../components/Comments.vue'
  import Hashtags from '../components/Hashtags.vue'
  import Reaction from '../components/Reaction.vue'
  export default {
    components: { Reaction, Hashtags, Banner, Comments },
    data: () => {
      return {
        comments: [
          {
            user: '안녕 나 응애',
            avatar: 'https://en.gravatar.com/userimage/100383909/61e19fd27a19e420a4251098c3939def.png',
            comment: '어머 제가 있던 테이블이 제일 반응이 좋았나보네요🤭 우짤래미님도 아시겠지만 저도 일반인 몸매 그 이상도 이하도 아니잖아요?! 그런 제가 기꺼이 도전해봤는데 생각보다 괜찮았어요! 오늘 중으로 라이브 리뷰 올라온다고 하니 꼭 봐주세용~!',
            likes: 5,
            reply: 5,
            replies: [
              {
                user: 'ㅇㅅㅇ',
                avatar: 'https://en.gravatar.com/userimage/100383909/61e19fd27a19e420a4251098c3939def.png',
                comment: '오 대박! 라이브 리뷰 오늘 올라온대요? 챙겨봐야겠다',
                likes: 5,
                reply: 5,
                replies: []
              }
            ]
          }
        ]
      }
    }
  }
</script>