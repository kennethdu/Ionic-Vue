<template>
  <div class="home">
    <img alt="r/pics logo" src="https://styles.redditmedia.com/t5_2qh0u/styles/bannerPositionedImage_ssrvude96kzz.png">
    <RedditList />
  </div>
</template>

<script>
// @ is an alias to /src
import RedditList from '@/components/RedditList.vue'

export default {
  name: 'home',
  components: {
    RedditList
  }
}
</script>
