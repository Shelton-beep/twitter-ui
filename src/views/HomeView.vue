<template>
  <div class="home">
    <TweetCard v-for="tweet in tweets" :tweet="tweet" :key="tweet._id" />
  </div>
</template>

<script>
import { ref } from "vue"
import TweetCard from "../components/TweetCard"
import vweets from "../vweets"

export default {
  setup() {
    const tweets = ref(vweets);

    return {
      tweets
    };

  },
  components:{
    TweetCard
  }
};
</script>
