<template>
  <div class="container">
    <Navbar />
    <div class="mid-column">
      <!-- title -->
      <div class="page-title">
        <div class="vector">
          <a href="#" class="vector-btn">
            <img src="../assets/vector.png" alt="">
          </a>
        </div>
        <div class="user-name">
          <h5>John Doe</h5>
          <div class="post-count">
            25 推文
          </div>
        </div>
      </div>
      <div class="scrollbar">
        <UserTop />
        <div class="user-tab">
          <UserTab />
        </div>
        <div class="post-list">
          <PostList />
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
import UserTop from '../components/UserTop.vue'
import UserTab from '../components/UserTab.vue'
import PostList from '../components/PostList.vue'
import ReplyList from '../components/ReplyList.vue'

export default {
  components: {
    Navbar,
    Recommended,
    UserTop,
    UserTab,
    PostList,
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
  .vector {
    display: flex;
    align-items: center;
  }

  .vector-btn {
    display: inline-block;
    margin-right: 16px;
    line-height: 24px;
  }

  .vector-btn img {
    display: block;
  }

  .mid-column {
    display: flex;
    flex-direction: column;
    flex: 1;
    margin-left: 202px;
    margin-right: 24px;
    height: 100%;
    border-left: 1px solid #E6ECF0;
    border-right: 1px solid #E6ECF0;
  }

  .page-title {
    display: flex;
    padding: 24px 0 24px 23px;
    text-align: left;
    color: #171725;
    border-bottom: 1px solid #E6ECF0;
  }

  .post-count {
    font-weight:500;
    font-size: 13px;
    color: #6C757D;
  }

  .create-post {
    height: 136px;
  }
  .scrollbar {
    overflow-y: scroll;
  }

  .post-list {
    display: none;
    height: 100%;
  }

  .reply-list {
    /* display: none; */
    height: 100%;
  }

  .recommended {
    margin-top: 16px;
  }

  .user-tab {
    margin-top: 18px;
    border-bottom: 1px solid #E6ECF0;
  }
</style>