<template>
  <div class="home">
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
