<template>
  <div class="posts-container">
    <ReplyModal 
      :show-modal="isShowModal"
      @close-modal="closeModal"
    />
    <div class="post">
      <div class="post-avatar">
        <div class="user-img"></div>
      </div>
      <div class="post-wrapper">
        <div class="post-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="post-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
        <div class="post-icons">
          <div
            class="post-icons-comments"
            @click="showModal"
          >
            <img src="../assets/icon_reply.png" alt="" class="icon"/>
            <span class="post-icons-comments-count count">14</span>
          </div>
          <div class="post-icons-likes">
            <img src="../assets/icon_like.png" alt="" class="icon"/>
            <span class="post-icons-likes-count count">14</span>
          </div>
        </div>
      </div>
    </div>

    <div class="post">
      <div class="post-avatar">
        <div class="user-img"></div>
      </div>
      <div class="post-wrapper">
        <div class="post-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="post-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
        <div class="post-icons">
          <div class="post-icons-comments">
            <img src="../assets/icon_reply.png" alt="" class="icon"/>
            <span class="post-icons-comments-count count">14</span>
          </div>
          <div class="post-icons-likes">
            <img src="../assets/icon_like.png" alt="" class="icon"/>
            <span class="post-icons-likes-count count">14</span>
          </div>
        </div>
      </div>
    </div>

    <div class="post">
      <div class="post-avatar">
        <div class="user-img"></div>
      </div>
      <div class="post-wrapper">
        <div class="post-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="post-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
        <div class="post-icons">
          <div class="post-icons-comments">
            <img src="../assets/icon_reply.png" alt="" class="icon"/>
            <span class="post-icons-comments-count count">14</span>
          </div>
          <div class="post-icons-likes">
            <img src="../assets/icon_like.png" alt="" class="icon"/>
            <span class="post-icons-likes-count count">14</span>
          </div>
        </div>
      </div>
    </div>

    <div class="post">
      <div class="post-avatar">
        <div class="user-img"></div>
      </div>
      <div class="post-wrapper">
        <div class="post-avatar-info">
          <div class="name">Apple</div>
          <div class="id">@apple</div>
          <span>・</span>
          <div class="created-time">3小時</div>
        </div>
        <div class="post-content">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta
          quisquam, facilis aperiam qui nisi fugit. Earum quidem nobis vel fugit
          molestiae, deleniti facere praesentium natus illum aut iusto quibusdam
          iste! Ad eveniet ex molestias nemo! Necessitatibus, laboriosam
          nesciunt? Nesciunt doloribus quaerat a quia molestiae reiciendis ipsa
          ullam officia dolores ea? Eligendi, dolores blanditiis dicta
          aspernatur et eum. Recusandae, nostrum omnis?
        </div>
        <div class="post-icons">
          <div class="post-icons-comments">
            <img src="../assets/icon_reply.png" alt="" class="icon"/>
            <span class="post-icons-comments-count count">14</span>
          </div>
          <div class="post-icons-likes">
            <img src="../assets/icon_like.png" alt="" class="icon"/>
            <span class="post-icons-likes-count count">14</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ReplyModal from '../components/ReplyModal.vue'

export default {
  components: {
    ReplyModal
  },
  data() {
    return {
      isShowModal: false
    }
  },
  methods: {
    showModal() {
      this.isShowModal = true
    },
    closeModal() {
      this.isShowModal = false
    }
  }
}
</script>

<style scoped>
.posts-container {
  height: 100%;
}

.post {
  display: flex;
  padding: 16px 24px;
  border-bottom: 1px solid  #E6ECF0;
}

.user-img {
  width: 50px;
  height: 50px;
  margin-right: 8px;
  border-radius: 50px;
  background: gray;
}

.post-avatar-info {
  display: flex;
  margin-bottom: 8px;
}

.name {
  margin-right: 8px;
}

.id,
.id ~ span,
.created-time {
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  color: #6C757D;
}

.post-content {
  margin-bottom: 9px;
  text-align: left;
  font-weight: 400;
  font-size: 16px;
  line-height: 26px;
  color: #171725;
}

.post-icons {
  display: flex;
  align-items: center;
}

.post-icons-comments {
  display: flex;
  margin-right: 41.3px;
  cursor: pointer;
}

.post-icons-likes {
  display: flex;
  cursor: pointer;
}

.icon {
  margin-right: 9.44px;
}

.count {
  font-weight: 600;
  font-size: 14px;
  line-height: 14px;
  color: #6C757D;
}
</style>