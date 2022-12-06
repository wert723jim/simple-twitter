<template>
  <div 
    :class="['modal-container', {show: isShow}]"
  >
    <div class="modal-content">
      <div
        class="modal-header"
        @click="closeModal"
      >
        <img src="../assets/close_btn.png" alt="" class="close-btn">
      </div>
      
      <div class="modal-body">
        <div class="post-review">
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
              iste!
            </div>
            <div class="reply-to">
              回覆給 <span>@apple</span>
            </div>
          </div>
        </div>
        <div class="reply-content">
          <div class="avatar-img">
            <div class="user-img"></div>
          </div>
          <div class="text-content">
            <textarea name="" id="" cols="30" rows="5" placeholder="今天想說什麼?"></textarea>
          </div>
        </div>
      </div>
      <div class="modal-footer">
        <button class="btn">
          推文
        </button>
      </div>
      <div class="modal-background">

      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  props: {
    showModal: {
      type: Boolean,
      default: false
    }
  },
  watch: {
    showModal(newValue) {
      this.isShow = newValue
    }
  },
  data() {
    return {
      isShow: this.showModal
    }
  },
  methods: {
    closeModal() {
      this.isShow = false
      this.$emit("close-modal")
    }
  }
}
</script>

<style scoped>
  .modal-container {
    /* 預設為不顯示 */
    display: none;
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    padding-top: 56px;
    z-index: 1055;
  }

  .modal-container.show {
    display: block;
  }

  .modal-content {
    z-index: 1;
    margin: 0 auto;
    width: 634px;
    background: #FFFFFF;
    border-radius: 14px;
  }

  .modal-header {
    padding: 16px 15px;
    text-align: left;
    border-bottom: 1px solid #E6ECF0;
  }

  .close-btn {
    cursor: pointer;
  }

  .modal-body {
    display: flex;
    flex-direction: column;
    padding: 16px 24px;
  }

  .post-review {
    display: flex;
  }

  .post-wrapper {
    margin-left: 8px;
  }

  .post-avatar {
    position: relative;
  }

  .post-avatar::after {
    content: '';
    position: absolute;
    border: 1px solid #B5B5BE;
    top: 66px;
    bottom: 0;
  }

  .user-img {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    background: gray;
  }

  .post-content {
    margin-bottom: 9px;
    text-align: left;
    font-weight: 400;
    font-size: 16px;
    line-height: 26px;
    color: #171725;
  }

  .reply-to {
    margin-bottom: 15px;
    text-align: left;
    color: #657786;
    font-size: 14px;
  }

  .reply-to span {
    color:#FF6600;
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

  .user-img {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    background: #FF6600;
  }
  
  .text-content {
    text-align: left;
    width: 100%;

  }

  .reply-content {
    display: flex;
    padding-top: 16px;
  }

  textarea {
    padding: 8px;
    resize: none;
    border: none;
    width: 100%;
    font-weight: 700;
    font-size: 16px;
    line-height: 26px;
    color: #6C757D;
  }

  textarea:focus {
    outline: none;
  }

  .modal-footer {
    text-align: right;
    padding-right: 16px;
    padding-bottom: 16px;
  }

  .btn {
    right: 24.69px;
    bottom: 16px;
    width: 60px;
    height: 40px;
    border: none;
    border-radius: 50px;
    background: #FF6600;
    color: white;
    cursor: pointer;
  }

  .modal-background {
    z-index: -1;
    position:absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 100%;
    background: #171725;
    opacity: .4
  }
</style>