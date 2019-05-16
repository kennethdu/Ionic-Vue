<template>
  <div class="hello">
    <ion-header>
      <ion-toolbar>
        <ion-title>Reddit Clone /r/pics</ion-title>
      </ion-toolbar>
    </ion-header>
    <!-- <ion-list> -->
      <ion-card
        v-for="post in posts"
        :key="post.data.id"
        @click="handleClick(post.data.preview.images[0].source.url)"
      >
        <img :src="post.data.thumbnail" alt="thumb" class="thumbnail">
        <h2 text-wrap id="title">{{ post.data.title }}</h2>
        <ion-card-subtitle text-wrap>User: {{ post.data.author }}</ion-card-subtitle>

      </ion-card>
    <!-- </ion-list> -->
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "RedditList",
  props: {
    msg: String
  },
  mounted() {
    axios
      .get("https://www.reddit.com/r/pics.json?raw_json=1")
      .then(response => {
        // console.log(response.data.data.children);
        this.posts = response.data.data.children;
      });
  },
  data() {
    return {
      posts: []
    };
  },
  methods: {
    handleClick(imageSrc) {
      this.$router.push({ name: "about", params: { imageSrc } });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.thumbnail {
  width: 90px;
  height: 90px;
  border-radius: 30px;
  margin-top: 10px;
  margin-bottom: 10px;
  display: inline;
}

#title {
  text-align: center;
  margin-bottom: 10px;
}
</style>
