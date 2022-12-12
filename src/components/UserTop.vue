<template>
  <div class="user-container">
    <UserEditModal
      :show-modal="isShowModal"
      @close-modal="closeModal"
    />
    <div class="user-img">
      <div class="avatar-img">
        <img src="../assets/user_background.png" alt="" class="background-img">
        <div class="user-avatar-img">
          <div class="img"></div>
        </div>
      </div>
      <button
        class="edit-btn"
        @click="showUserEditModal"
      >
        編輯個人資料
      </button>
    </div>
    <div class="user-info">
      <h5>
        John Doe
      </h5>
      <div class="user-id">
        @heyjohn
      </div>
      <div class="user-intro">
        Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
      </div>
      <div class="user-counts">
        <div class="following-counts">
          <router-link
            :to="{name: 'user-followers', params: {id: 1}}"
          >
            <span class="counts">34個</span>
          </router-link>
          <span>跟隨中</span>
        </div>
        <div class="follower-counts">
          <router-link
            :to="{name: 'user-followings', params: {id: 1}}"
          >
            <span class="counts">24個</span>
          </router-link>
          <span>跟隨者</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import UserEditModal from '../components/UserEditModal.vue'
export default {
  components: {
    UserEditModal
  },
  data() {
    return {
      isShowModal: false
    }
  },
  methods: {
    showUserEditModal() {
      this.isShowModal = true
    },
    closeModal() {
      this.isShowModal = false
    }
  }
}
</script>

<style scoped>
  .user-img {
    text-align: right;
  }
  .avatar-img {
    position: relative;
  }

  .background-img {
    display: block;
    width: 100%;
    height: 100%;
  }

  .user-avatar-img {
    position: absolute;
    z-index: 2;
    bottom: -70px;
    left: 16px;
  }

  .img {
    width: 140px;
    height: 140px;
    border: 4px solid #FFFFFF;
    border-radius: 140px;
    background: black;
  }

  .edit-btn {
    margin: 16px 16px 0 0;
    width: 128px;
    height: 40px;
    background: #FFFFFF;
    color: #FF6600;
    border: 1px solid #FF6600;
    border-radius: 50px;
    cursor: pointer;
  }

  .user-info {
    margin-top: 16px;
    padding: 0 16px;
    text-align: left;
  }

  .user-id {
    margin-bottom: 6px;
    font-size: 14px;
    font-weight: 400;
    line-height: 22px;
    color: #6C757D;
  }

  .user-intro {
    margin-bottom: 8px;
  }

  .user-counts {
    display: flex;
    font-size: 14px;
    color: #6C757D;
  }

  .following-counts {
    margin-right: 20px;
  }

  .counts {
    color: #171725;
  }
</style>