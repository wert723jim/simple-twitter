<template>
  <div class="container">
    <div class="navbar">
      <Navbar />
    </div>
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
      <FollowTab />
      <div class="scrollbar">
        <FollowersList />
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
import FollowTab from '../components/FollowTab.vue'
import FollowersList from '../components/FollowersList.vue'


export default {
  components: {
    Navbar,
    Recommended,
    FollowTab,
    FollowersList
  },
  data() {
    return {
      chosenTab: 'tweets'
    }
  },
  methods: {
    displayChosenTab(tabName) {
      this.chosenTab = tabName
    }
  }
}
</script>

<style scoped>
  .container {
    display: flex;
    height: 100%;
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
    margin: 0 24px;
    height: 100%;
    border-left: 1px solid #E6ECF0;
    border-right: 1px solid #E6ECF0;
  }

  .page-title {
    display: flex;
    align-items: center;
    padding-left: 23px;
    height: 74px;
    text-align: left;
    color: #171725;
    border-bottom: 1px solid #E6ECF0;
  }

  .scrollbar {
    flex: 1;
    overflow-y: scroll;
  }

  .recommended {
    margin-top: 16px;
  }

</style>