<template>
<div class="container">
  <div class="nav">
    <Navbar />
  </div>
  <div class="mid-column">
    <!-- title -->
    <div class="page-title">
      <h4>首頁</h4>
    </div>
    <div class="create-post">
      <CreatePost />
    </div>
    <div class="post-list">
      <PostList />
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
import CreatePost from '../components/CreatePost.vue'
import PostList from '../components/PostList.vue'

export default {
  components: {
    Navbar,
    Recommended,
    CreatePost,
    PostList
  },
}
</script>

<style scoped>
  .container {
    display: flex;
    height: 100%;
  }

  .mid-column {
    display: flex;
    flex-direction: column;
    flex: 1;
    margin: 0 24px;
    height: 100%;
    border-left: 1px solid #E6ECF0;
    border-right : 1px solid #E6ECF0;
  }

  .page-title {
    display: flex;
    align-items: center;
    height: 74px;
    padding-left:23px;
    text-align: left;
    color: #171725;
    border-bottom: 1px solid #E6ECF0;
  }

  .create-post {
    height: 136px;
  }

  .post-list {
    flex: 1;
    overflow-y: scroll;
  }

  .recommended {
    margin-top: 16px;
  }
</style>