<template>
<div class="container">
  <Navbar />
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
    padding: 24px 0 24px 23px;
    text-align: left;
    color: #171725;
    border-bottom: 1px solid #E6ECF0;
  }

  .create-post {
    height: 136px;
  }

  .post-list {
    height: 100%;
    overflow-y: scroll;
  }

  .recommended {
    margin-top: 16px;
  }
</style>