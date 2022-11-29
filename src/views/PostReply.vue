<template>
  <div class="container">
    <Navbar />
    <div class="mid-column">
      <!-- title -->
      <div class="page-title">
        <a href="#" class="vector-btn">
          <img src="../assets/vector.png" alt="">
        </a>
        <h4>推文</h4>
      </div>
      <div class="scrollbar">
        <div class="post-content">
          <Post />
        </div>
        <div class="reply-list">
          <ReplyList />
        </div>
      </div>
    </div>
    <div class="recommended">
      <Recommended />
    </div>
  </div>
    
</template>

<script>
import Navbar from '../components/Navbar.vue'
import Recommended from '../components/Recomended.vue'
import Post from '../components/Post.vue'
import ReplyList from '../components/ReplyList.vue'

export default {
  components: {
    Navbar,
    Recommended,
    Post,
    ReplyList
  }
}
</script>

<style scoped>
  .container {
    position: relative;
    display: flex;
    height: 100%;
    justify-items: space-between;
  }
/* 返回鍵 */
  .vector-btn {
    display: flex;
    margin-right: 16px;
    line-height: 24px;
  }

  .mid-column {
    display: flex;
    flex-direction: column;
    flex: 1;
    margin-left: 202px;
    margin-right: 24px;
    height: 100%;
    border-left: 1px solid #E6ECF0;
    border-right : 1px solid #E6ECF0;
  }

  .page-title {
    display: flex;
    padding: 24px 0 24px 23px;
    text-align: left;
    color: #171725;
    border-bottom: 1px solid #E6ECF0;
  }

  .create-post {
    height: 136px;
  }
  .scrollbar {
    overflow-y: scroll;
  }

  .post-list {
    height: 100%;
  }

  .recommended {
    margin-top: 16px;
  }
</style>