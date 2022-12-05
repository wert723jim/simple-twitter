<template>
  <nav class="nav">
    <TweetModal 
      :show-modal="isShow"
      @close-modal="closeModal"
    />
    <img src="../assets/logo.png" alt="" class="brand-logo">
    <div class="nav-tools">
      <div class="nav-list">
        <ul class="list-items">
          <li class="item">
            <router-link to="/main" class="item-link">
              <img src="../assets/home_hollow_2x.png" alt="" class="item-img">
              <img src="../assets/home_filled_2x.png" alt="" class="item-img-selected">
              首頁
            </router-link>
          </li>
          <li class="item">
            <router-link to="/user/1" class="item-link">
              <img src="../assets/info_hollow_2x.png" alt="" class="item-img">
              <img src="../assets/info_filled_2x.png" alt="" class="item-img-selected">
              個人資料
            </router-link>
          </li>
          <li class="item">
            <router-link to="/setting" class="item-link">
              <img src="../assets/setting_hollow_2x.png" alt="" class="item-img">
              <img src="../assets/setting_filled_2x.png" alt="" class="item-img-selected">
              設定
            </router-link>
          </li>
        </ul>
      </div>
      <div class="nav-btn">
        <button
          class="btn"
          @click="showModal"
        >
          推文
        </button>
      </div>
    </div>
    <div class="item">
      <a href="#" class="item-link">
        <img src="../assets/logout_hollow_2x.png" alt="" class="item-img">
        登出
      </a>
    </div>
  </nav>
</template>

<script>
import TweetModal from '../components/TweetModal.vue'
export default {
  components: {
    TweetModal,
  },
  data() {
    return {
      isShow: false
    }
  },
  methods: {
    showModal() {
      this.isShow = true
    },
    closeModal(close) {
      this.isShow = close
    }
  }
}
</script>

<style scoped>
  .nav {
    display: flex;
    flex-direction: column;
    /* position: fixed; */
    z-index: 999;
    width: 178px;
    height: 100%;
    margin: 0;
    text-align: start;
    background: #FFFFFF;
  }

  .brand-logo {
    width: 40px;
    height: 40px;
    margin: 13px 0 0 13px;
  }

  .nav-tools {
    /* 占滿剩餘空間 */
    flex: 1;
  }

  .nav-list {
    margin-bottom: 8px;
  }

  .item {
    padding: 16px;
    font-size: 18px;
  }

  .item-img,
  .item-img-selected {
    width: 24px;
    height: 24px;
    margin-right: 16px;
  }

  .item-img-selected {
    display: none;
  }

  .item-link {
    display: flex;
    align-items: center;
    color: black;
  }

  .item-link.active {
    color: #FF6600;
  }

  .item-link.active .item-img-selected {
    display: block;
  }
  .item-link.active .item-img {
    display: none;
  }

  .btn {
    width: 100%;
    height: 46px;
    border: none;
    border-radius: 50px;
    background: #FF6600;
    font-size: 20px;
    color: #FFFFFF;
    cursor: pointer;
  }

</style>